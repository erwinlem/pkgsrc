# $NetBSD: Makefile,v 1.17 2019/08/11 13:21:06 wiz Exp $
#

DISTNAME=	Geo-ShapeFile-2.66
PKGNAME=	p5-${DISTNAME}
PKGREVISION=	1
CATEGORIES=	geography perl5
MASTER_SITES=	${MASTER_SITE_PERL_CPAN:=Geo/}

MAINTAINER=	wen@NetBSD.org
HOMEPAGE=	https://metacpan.org/release/Geo-ShapeFile
COMMENT=	Perl extension for handling ESRI GIS Shapefiles
LICENSE=	${PERL5_LICENSE}

DEPENDS+=	p5-Tree-R>=0:../../devel/p5-Tree-R
DEPENDS+=	p5-autovivification>=0:../../devel/p5-autovivification

PERL5_PACKLIST=	auto/Geo/ShapeFile/.packlist

.include "../../lang/perl5/module.mk"
.include "../../mk/bsd.pkg.mk"
