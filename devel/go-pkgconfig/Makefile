# $NetBSD: Makefile,v 1.1 2020/04/28 13:28:04 nikita Exp $

GITHUB_TAG=	cea12a0fd2454f031cbce19aec911c1e92af25da
DISTNAME=	go-pkgconfig-0.0.0.20170226
CATEGORIES=	devel
MASTER_SITES=	${MASTER_SITE_GITHUB:=xlab/}
GITHUB_PROJECT=	pkgconfig

MAINTAINER=	nikita@NetBSD.org
HOMEPAGE=	https://github.com/xlab/pkgconfig/
COMMENT=	Go clone of pkg-config(1)
LICENSE=	mit

GO_SRCPATH=	github.com/xlab/pkgconfig
GO_DIST_BASE=	pkgconfig-${GITHUB_TAG}

.include "../../lang/go/go-package.mk"
.include "../../mk/bsd.pkg.mk"
