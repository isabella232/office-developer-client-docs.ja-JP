---
title: Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35cab114da6536ea1a0123e0da2541dd69125824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877885"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="6de7a-102">Microsoft OLE DB Persistence Provider (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="6de7a-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="6de7a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6de7a-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="6de7a-p101">Microsoft OLE DB Persistence Provider を使用すると、[Recordset](recordset-object-ado.md) オブジェクトをファイルに保存し、後でその **Recordset** オブジェクトをファイルから復元できます。スキーマ情報、データ、および保留中の変更が保持されます。</span><span class="sxs-lookup"><span data-stu-id="6de7a-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="6de7a-106">**Recordset** は、独自の ADTG (Advanced Data Table Gram) 形式または公開されている XML (Extensible Markup Language) 形式で保存できます。</span><span class="sxs-lookup"><span data-stu-id="6de7a-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="6de7a-107">プロバイダー キーワード</span><span class="sxs-lookup"><span data-stu-id="6de7a-107">Provider Keyword</span></span>

<span data-ttu-id="6de7a-108">このプロバイダーを呼び出すには、接続文字列で次のキーワードと値を指定します。</span><span class="sxs-lookup"><span data-stu-id="6de7a-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="6de7a-109">エラー</span><span class="sxs-lookup"><span data-stu-id="6de7a-109">Errors</span></span>

<span data-ttu-id="6de7a-110">このプロバイダーからの次のエラーが発生し、アプリケーションで検出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="6de7a-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6de7a-111">定数</span><span class="sxs-lookup"><span data-stu-id="6de7a-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="6de7a-112">説明</span><span class="sxs-lookup"><span data-stu-id="6de7a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6de7a-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="6de7a-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="6de7a-114">開かれたファイルの形式が有効な形式 (ADTG 形式または XML 形式) ではありません。</span><span class="sxs-lookup"><span data-stu-id="6de7a-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6de7a-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="6de7a-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="6de7a-116">保存する <strong>Recordset</strong> オブジェクトには、保存を妨げる特性があります。</span><span class="sxs-lookup"><span data-stu-id="6de7a-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6de7a-117">解説</span><span class="sxs-lookup"><span data-stu-id="6de7a-117">Remarks</span></span>

<span data-ttu-id="6de7a-118">Microsoft OLE DB Persistence Provider は動的プロパティを公開しません。</span><span class="sxs-lookup"><span data-stu-id="6de7a-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="6de7a-119">現在、パラメーター化された階層 **Recordset** オブジェクトのみ保存できません。</span><span class="sxs-lookup"><span data-stu-id="6de7a-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="6de7a-120">**Recordset** オブジェクトの永続的保存の詳細については、「 [レコードセットの保存の詳細](more-about-recordset-persistence.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6de7a-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="6de7a-121">ストリームが使用すると、**レコード セット**を開く必要がありますパラメーターが指定されていない、 **Open**メソッドの*Source*パラメーター以外の場合。</span><span class="sxs-lookup"><span data-stu-id="6de7a-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

