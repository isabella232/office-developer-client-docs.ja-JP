---
title: Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4045445120d42f1ca88fce22ce566fc970fce28b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715509"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="2d1d6-102">Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="2d1d6-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="2d1d6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="2d1d6-p101">Microsoft OLE DB Persistence Provider を使用すると、[Recordset](recordset-object-ado.md) オブジェクトをファイルに保存し、後でその **Recordset** オブジェクトをファイルから復元できます。スキーマ情報、データ、および保留中の変更が保持されます。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="2d1d6-106">**Recordset** は、独自の ADTG (Advanced Data Table Gram) 形式または公開されている XML (Extensible Markup Language) 形式で保存できます。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="2d1d6-107">プロバイダー キーワード</span><span class="sxs-lookup"><span data-stu-id="2d1d6-107">Provider Keyword</span></span>

<span data-ttu-id="2d1d6-108">このプロバイダーを呼び出すには、接続文字列で次のキーワードと値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="2d1d6-109">エラー</span><span class="sxs-lookup"><span data-stu-id="2d1d6-109">Errors</span></span>

<span data-ttu-id="2d1d6-110">このプロバイダーからの次のエラーが発生し、アプリケーションで検出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d1d6-111">定数</span><span class="sxs-lookup"><span data-stu-id="2d1d6-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d1d6-112">説明</span><span class="sxs-lookup"><span data-stu-id="2d1d6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d1d6-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="2d1d6-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="2d1d6-114">開かれたファイルの形式が有効な形式 (ADTG 形式または XML 形式) ではありません。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d1d6-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="2d1d6-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="2d1d6-116">保存する <strong>Recordset</strong> オブジェクトには、保存を妨げる特性があります。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2d1d6-117">解説</span><span class="sxs-lookup"><span data-stu-id="2d1d6-117">Remarks</span></span>

<span data-ttu-id="2d1d6-118">Microsoft OLE DB Persistence Provider は動的プロパティを公開しません。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="2d1d6-119">現在、パラメーター化された階層 **Recordset** オブジェクトのみ保存できません。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="2d1d6-120">**Recordset** オブジェクトの永続的保存の詳細については、「 [レコードセットの保存の詳細](more-about-recordset-persistence.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="2d1d6-121">ストリームが使用すると、**レコード セット**を開く必要がありますパラメーターが指定されていない、 **Open**メソッドの*Source*パラメーター以外の場合。</span><span class="sxs-lookup"><span data-stu-id="2d1d6-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

