---
title: ConvertToString メソッド (RDS)
TOCTitle: ConvertToString method (RDS)
ms:assetid: dc6381e4-98c8-badc-ad8c-87c70574a8a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250113(v=office.15)
ms:contentKeyID: 48548136
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2c589339eb838f944ce4443c19a787eafb01c3dd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717728"
---
# <a name="converttostring-method-rds"></a><span data-ttu-id="0c7e2-102">ConvertToString メソッド (RDS)</span><span class="sxs-lookup"><span data-stu-id="0c7e2-102">ConvertToString method (RDS)</span></span>

<span data-ttu-id="0c7e2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="0c7e2-104">[Recordset](recordset-object-ado.md) を、レコードセットのデータを表す MIME 文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-104">Converts a [Recordset](recordset-object-ado.md) to a MIME string that represents the recordset data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7e2-105">構文</span><span class="sxs-lookup"><span data-stu-id="0c7e2-105">Syntax</span></span>

<span data-ttu-id="0c7e2-106">*DataFactory*。ConvertToString (*レコード セット*)</span><span class="sxs-lookup"><span data-stu-id="0c7e2-106">*DataFactory*.ConvertToString(*Recordset*)</span></span>

## <a name="parameters"></a><span data-ttu-id="0c7e2-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c7e2-107">Parameters</span></span>

|<span data-ttu-id="0c7e2-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0c7e2-108">Parameter</span></span>|<span data-ttu-id="0c7e2-109">説明</span><span class="sxs-lookup"><span data-stu-id="0c7e2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0c7e2-110">*DataFactory*</span><span class="sxs-lookup"><span data-stu-id="0c7e2-110">*DataFactory*</span></span> |<span data-ttu-id="0c7e2-111">[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-111">An object variable that represents an [RDSServer.DataFactory](datafactory-object-rdsserver.md) object.</span></span>|
|<span data-ttu-id="0c7e2-112">*Recordset*</span><span class="sxs-lookup"><span data-stu-id="0c7e2-112">*Recordset*</span></span> |<span data-ttu-id="0c7e2-113">**Recordset** オブジェクトを表すオブジェクト変数です。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-113">An object variable that represents a **Recordset** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0c7e2-114">解説</span><span class="sxs-lookup"><span data-stu-id="0c7e2-114">Remarks</span></span>

<span data-ttu-id="0c7e2-115">.asp ファイルでは、 **ConvertToString** を使用して **Recordset** をサーバーで生成された HTML ページに埋め込み、クライアント コンピューターに転送します。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-115">With .asp files, use **ConvertToString** to embed the **Recordset** in an HTML page generated on the server to transport it to a client computer.</span></span>

<span data-ttu-id="0c7e2-116">**ConvertToString** は、最初に **Recordset** を Cursor Service テーブルに読み込み、次に MIME 形式のストリームを生成します。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-116">**ConvertToString** first loads the **Recordset** into the Cursor Service tables, and then generates a stream in MIME format.</span></span>

<span data-ttu-id="0c7e2-p101">クライアントでは、リモート データ サービスで MIME 文字列を変換し、完全に機能する **Recordset** に戻すことができます。1 行が 1,024 バイト以下で行数が 400 行未満のデータは、適切に処理されます。BLOB データおよび大きな結果セットを HTTP でストリーム配信する場合は、このメソッドを使用しないでください。文字列はワイヤー圧縮されないため、オンライン向けに最適化されたテーブルグラム形式と比較して、HTTP で大きなデータ セットを転送するにはかなりの時間がかかります。テーブルグラム形式は、リモート データ サービスのネイティブ転送プロトコル形式として定義され、展開されています。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-p101">On the client, Remote Data Service can convert the MIME string back into a fully functioning **Recordset**. It works well for handling fewer than 400 rows of data with no more than 1024 bytes width per row. You shouldn't use it for streaming BLOB data and large result sets over HTTP. No wire compression is performed on the string, so very large data sets will take considerable time to transport over HTTP when compared to the wire-optimized tablegram format defined and deployed by Remote Data Service as its native transport protocol format.</span></span>

> [!NOTE]
> <span data-ttu-id="0c7e2-p102">[!メモ] Active Server Pages を使用して、生成された MIME 文字列をクライアントの HTML ページに埋め込む場合、2.0 より前のバージョンの VBScript では、文字列のサイズが 32K に制限されていることに注意してください。この制限を超えると、エラーが返されます。.asp ファイルで MIME の埋め込みを使用するときは、クエリの適用範囲を比較的小さくするようにしてください。この問題を回避するには、[Microsoft ダウンロード センター](https://www.microsoft.com/download/default.aspx)から最新バージョンの VBScript をダウンロードしてください。</span><span class="sxs-lookup"><span data-stu-id="0c7e2-p102">If you are using Active Server Pages to embed the resulting MIME string in a client HTML page, be aware that versions of VBScript earlier than version 2.0 limit the string's size to 32K. If this limit is exceeded, an error is returned. Keep the query scope relatively small when using MIME embedding via .asp files. To fix this, download the latest version of VBScript from the [Microsoft Download Center](https://www.microsoft.com/download/default.aspx).</span></span>


