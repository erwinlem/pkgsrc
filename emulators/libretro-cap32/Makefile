# $NetBSD: Makefile,v 1.4 2020/05/26 09:45:13 nia Exp $

DISTNAME=	libretro-cap32-20190128
CATEGORIES=	emulators
MASTER_SITES=	${MASTER_SITE_GITHUB:=libretro/}
GITHUB_TAG=	1a8bcf4d68b633bb8e92e20da460ac7618e8b950

MAINTAINER=	pkgsrc-users@NetBSD.org
HOMEPAGE=	https://docs.libretro.com/library/caprice32/
COMMENT=	Libretro core based on the Caprice32 Amstrad CPC emulator
LICENSE=	gnu-gpl-v2

USE_TOOLS+=	gmake
USE_LANGUAGES=	c99

OPSYSVARS+=	SOEXT
SOEXT.Darwin=	dylib
SOEXT.*=	so
PLIST_SUBST+=	SOEXT=${SOEXT}

.include "../../mk/endian.mk"

.if ${MACHINE_ENDIAN} == "big"
CFLAGS+=	-DMSB_FIRST
.endif

BUILDLINK_TRANSFORM.SunOS+=	rm:-Wl,-version-script=link.T
BUILDLINK_TRANSFORM.SunOS+=	rm:-Wl,-no-undefined

INSTALLATION_DIRS+=	${PREFIX}/lib/libretro

do-install:
	${INSTALL_LIB} ${WRKSRC}/cap32_libretro.so \
	    ${DESTDIR}${PREFIX}/lib/libretro/cap32_libretro.so

.include "../../devel/zlib/buildlink3.mk"
.include "../../mk/bsd.pkg.mk"
