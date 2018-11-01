---
title: Source プロパティ (ADO Record)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e0157bc81e3f7efdb2227b5c5a9e2bc3642a7d2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883954"
---
# <a name="source-property-ado-record"></a><span data-ttu-id="6dab8-102">Source プロパティ (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="6dab8-102">Source Property (ADO Record)</span></span>


<span data-ttu-id="6dab8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6dab8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6dab8-104">[Record](record-object-ado.md) で表されるデータ ソースまたはオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="6dab8-104">Indicates the data source or object represented by the [Record](record-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="6dab8-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="6dab8-105">Settings and return values</span></span>

<span data-ttu-id="6dab8-106">**Record** が表すエンティティを示すバリアント型 ( **Variant** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="6dab8-106">Sets or returns a **Variant** value that indicates the entity represented by the **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dab8-107">解説</span><span class="sxs-lookup"><span data-stu-id="6dab8-107">Remarks</span></span>

<span data-ttu-id="6dab8-108">**Source**プロパティは、 **Record**オブジェクトの[Open](open-method-ado-record.md)メソッドの*Source*引数を返します。</span><span class="sxs-lookup"><span data-stu-id="6dab8-108">The **Source** property returns the *Source* argument of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="6dab8-109">このプロパティには絶対 URL または相対 URL の文字列を格納できます。</span><span class="sxs-lookup"><span data-stu-id="6dab8-109">It can contain an absolute or relative URL string.</span></span> <span data-ttu-id="6dab8-110">絶対 URL を使用すると、 [ActiveConnection](activeconnection-property-ado.md) プロパティを設定せずに、直接 **Record** オブジェクトを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="6dab8-110">An absolute URL can be used without setting the [ActiveConnection](activeconnection-property-ado.md) property to directly open the **Record** object.</span></span> <span data-ttu-id="6dab8-111">この場合、暗黙の **Connection** オブジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6dab8-111">An implicit **Connection** object is created in this case.</span></span>

<span data-ttu-id="6dab8-112">**Source** プロパティには、既に開いている **Recordset** への参照も格納でき、この参照は **Recordset** 内の現在の行を表す **Record** オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="6dab8-112">The **Source** property can also contain a reference to an already open **Recordset**, which opens a **Record** object representing the current row in the **Recordset**.</span></span>

<span data-ttu-id="6dab8-113">また、 **Source** プロパティには、プロバイダーから 1 つのデータ行を返す [Command](command-object-ado.md) オブジェクトへの参照も格納できます。</span><span class="sxs-lookup"><span data-stu-id="6dab8-113">The **Source** property could also contain a reference to a [Command](command-object-ado.md) object which returns a single row of data from the provider.</span></span>

<span data-ttu-id="6dab8-p102">**ActiveConnection** プロパティも設定する場合は、 **Source** プロパティはその接続範囲内に存在する同じオブジェクトを指している必要があります。たとえば、ツリー構造の名前空間では、 **Source** プロパティに絶対 URL が格納されている場合、接続文字列の URL で指定されたノードの範囲内に存在するノードを指している必要があります。 **Source** プロパティに相対 URL が格納されている場合、 **ActiveConnection** プロパティで設定されたコンテキスト内でのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="6dab8-p102">If the **ActiveConnection** property is also set, then the **Source** property must point to some object that exists within the scope of that connection. For example, in tree-structured namespaces, if the **Source** property contains an absolute URL, it must point to a node that exists inside the scope of the node identified by the URL in the connection string. If the **Source** property contains a relative URL, then it is validated within the context set by the **ActiveConnection** property.</span></span>

<span data-ttu-id="6dab8-117">**Source** プロパティは、 **Record** オブジェクトが閉じている場合は値の取得および設定が可能で、 **Record** オブジェクトが開いている場合は値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="6dab8-117">The **Source** property is read/write while the **Record** object is closed, and is read-only while the **Record** object is open.</span></span>

> [!NOTE]
> <span data-ttu-id="6dab8-118">[!メモ] http スキーマを使用している URL は自動的に [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="6dab8-118">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="6dab8-119">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6dab8-119">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


