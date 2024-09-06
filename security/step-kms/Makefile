PORTNAME=	step-kms
DISTVERSIONPREFIX=	v
DISTVERSION=	0.11.4
PORTREVISION=	1
CATEGORIES=	security

MAINTAINER=	mw@wipp.bayern
COMMENT=	Smallstep step-ca kms plugin
WWW=		https://smallstep.com/step-kms-plugin/

LICENSE=	APACHE20
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	pcsc-lite>0:devel/pcsc-lite
LIB_DEPENDS=	libpcsclite.so:devel/pcsc-lite
RUN_DEPENDS=	step:security/step-cli \
				RSA_SecurID_getpasswd:devel/libccid

USES=		go:modules

GO_MODULE=	github.com/smallstep/step-kms-plugin
GO_TARGET=	.:${PREFIX}/bin/step-kms-plugin
GO_BUILDFLAGS=	-ldflags "-w -X main.Version=${PORTVERSION}"

PLIST_FILES=	bin/step-kms-plugin

.include <bsd.port.mk>
