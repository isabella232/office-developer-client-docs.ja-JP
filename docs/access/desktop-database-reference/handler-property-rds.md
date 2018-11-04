---
title: Handler プロパティ (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98aeb3a56203fd5adbeb5b58a1298a7b1df98439
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950133"
---
# <a name="handler-property-rds"></a><span data-ttu-id="b1159-102">Handler プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="b1159-102">Handler property (RDS)</span></span>

<span data-ttu-id="b1159-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b1159-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1159-104">[RDSServer.DataFactory](datafactory-object-rdsserver.md)のおよび*ハンドラー*によって使用されるパラメーターの機能を拡張するサーバー側のカスタマイズ プログラム (ハンドラー) の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="b1159-104">Indicates the name of a server-side customization program (handler) that extends the functionality of the [RDSServer.DataFactory](datafactory-object-rdsserver.md), and any parameters used by the *handler*.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1159-105">構文</span><span class="sxs-lookup"><span data-stu-id="b1159-105">Syntax</span></span>

<span data-ttu-id="b1159-106">*DataControl*。ハンドラー =*文字列*</span><span class="sxs-lookup"><span data-stu-id="b1159-106">*DataControl*.Handler = *String*</span></span>

## <a name="parameters"></a><span data-ttu-id="b1159-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1159-107">Parameters</span></span>

|<span data-ttu-id="b1159-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1159-108">Parameter</span></span>|<span data-ttu-id="b1159-109">説明</span><span class="sxs-lookup"><span data-stu-id="b1159-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b1159-110">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="b1159-110">*DataControl*</span></span> |<span data-ttu-id="b1159-111">[RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b1159-111">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>|
|<span data-ttu-id="b1159-112">*String*</span><span class="sxs-lookup"><span data-stu-id="b1159-112">*String*</span></span> |<span data-ttu-id="b1159-113">ハンドラーおよびパラメーターをすべてコンマ (たとえば、「handlerName、parm1、parm2、...、 *N*のパラメーター」) の名前を含む**文字列**値。</span><span class="sxs-lookup"><span data-stu-id="b1159-113">A **String** value that contains the name of the handler and any parameters, all separated by commas (for example, "handlerName,parm1,parm2,...,parm *N*" ).</span></span>|

## <a name="remarks"></a><span data-ttu-id="b1159-114">解説</span><span class="sxs-lookup"><span data-stu-id="b1159-114">Remarks</span></span>

<span data-ttu-id="b1159-115">このプロパティは、カスタマイズをサポートしますが、この機能を使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1159-115">This property supports customization, a functionality that requires setting the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

<span data-ttu-id="b1159-p101">ハンドラーの名前とパラメーターは、コンマ (",") で区切ります。*String* 内にセミコロン (";") が含まれていると、予期できない結果が発生する場合があります。また、**IDataFactoryHandler** インターフェイスをサポートしているハンドラーであれば、独自に作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b1159-p101">The name of the handler and its parameters, if any, are separated by commas (","). Unpredictable behavior will result if a semicolon (";") appears anywhere within *String*. You can write your own handler, provided it supports the **IDataFactoryHandler** interface.</span></span>

<span data-ttu-id="b1159-p102">既定のハンドラー名は **MSDFMAP.Handler** であり、この既定パラメーターは **MSDFMAP.INI** という名のカスタマイズ ファイルです。このプロパティは、サーバー管理者が作成した別のカスタマイズ ファイルを呼び出すときに使います。</span><span class="sxs-lookup"><span data-stu-id="b1159-p102">The name of the default handler is **MSDFMAP.Handler**, and its default parameter is a customization file named **MSDFMAP.INI**. Use this property to invoke alternate customization files created by your server administrator.</span></span>

<span data-ttu-id="b1159-121">[ConnectionString](connectionstring-property-ado.md)プロパティのハンドラーとパラメーターを指定するのには、**ハンドラー**のプロパティを設定する代わりに、"\**ハンドラー =。 handlerName、parm1、parm2、...;*"です。</span><span class="sxs-lookup"><span data-stu-id="b1159-121">The alternative to setting the **Handler** property is to specify a handler and parameters in the [ConnectionString](connectionstring-property-ado.md) property; that is, "\**Handler=\*\*\*handlerName,parm1,parm2,...;*".</span></span>

