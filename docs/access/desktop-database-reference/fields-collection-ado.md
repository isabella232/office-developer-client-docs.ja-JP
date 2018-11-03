---
title: Fields コレクション (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 27741f8b1a07e4fae49818b72a7239d13d069cca
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931205"
---
# <a name="fields-collection-ado"></a><span data-ttu-id="952ed-102">Fields コレクション (ADO)</span><span class="sxs-lookup"><span data-stu-id="952ed-102">Fields collection (ADO)</span></span>


<span data-ttu-id="952ed-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="952ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="952ed-104">[Recordset](field-object-ado.md) オブジェクトまたは [Record](recordset-object-ado.md) オブジェクトのすべての [Field](record-object-ado.md) オブジェクトを格納します。</span><span class="sxs-lookup"><span data-stu-id="952ed-104">Contains all the [Field](field-object-ado.md) objects of a [Recordset](recordset-object-ado.md) or [Record](record-object-ado.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="952ed-105">備考</span><span class="sxs-lookup"><span data-stu-id="952ed-105">Remarks</span></span>

<span data-ttu-id="952ed-p101">**Recordset** オブジェクトには、 **Field** オブジェクトから構成される **Fields** コレクションがあります。各 **Field** オブジェクトは、 **Recordset** の 1 つの列に対応します。コレクションの **Refresh** メソッドを呼び出すと、 **Recordset** を開く前に [Fields](refresh-method-ado.md) コレクションにフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="952ed-p101">A **Recordset** object has a **Fields** collection made up of **Field** objects. Each **Field** object corresponds to a column in the **Recordset**. You can populate the **Fields** collection before opening the **Recordset** by calling the [Refresh](refresh-method-ado.md) method on the collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="952ed-109">[!メモ] <STRONG>Field</STRONG> オブジェクトの使用方法の詳細については、 <STRONG>Field</STRONG> オブジェクトのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="952ed-109">See the <STRONG>Field</STRONG> object topic for a more detailed explanation of how to use <STRONG>Field</STRONG> objects.</span></span></P>



<span data-ttu-id="952ed-110">**Fields** コレクションには、条件付きで [Field](append-method-ado.md) オブジェクトを作成しコレクションに追加する **Append** メソッド、および追加や削除を完了させる **Update** メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="952ed-110">The **Fields** collection has an [Append](append-method-ado.md) method, which provisionally creates and adds a **Field** object to the collection, and an **Update** method, which finalizes any additions or deletions.</span></span>

<span data-ttu-id="952ed-p102">**Record** オブジェクトには、 [FieldEnum](fieldenum.md) 定数でインデックスを設定できる 2 つの特別なフィールドがあります。1 つの定数は、 **Record** の既定のストリームを格納するフィールドにアクセスし、もう 1 つの定数は、 **Record** の絶対 URL 文字列を格納するフィールドにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="952ed-p102">A **Record** object has two special fields that can be indexed with [FieldEnum](fieldenum.md) constants. One constant accesses a field containing the default stream for the **Record**, and the other accesses a field containing the absolute URL string for the **Record**.</span></span>

<span data-ttu-id="952ed-p103">特定のプロバイダー (たとえば、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) は、 **Fields** コレクションに **Record** または **Recordset** の使用可能なフィールドのサブセットを追加できます。他のフィールドは、最初に名前で参照するか、コードでインデックス設定しない限り、コレクションに追加されません。</span><span class="sxs-lookup"><span data-stu-id="952ed-p103">Certain providers (for example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) may populate the **Fields** collection with a subset of available fields for the **Record** or **Recordset**. Other fields will not be added to the collection until they are first referenced by name or indexed by your code.</span></span>

<span data-ttu-id="952ed-p104">存在しないフィールドを名前で参照しようとすると、新しい **Field** オブジェクトが **Fields** コレクションに [Status](status-property-ado-field.md) が **adFieldPendingInsert** の状態で追加されます。 [Update](update-method-ado.md) を呼び出すと、プロバイダーで許容される限り、ADO によってデータ ソースに新しいフィールドが作成されます。</span><span class="sxs-lookup"><span data-stu-id="952ed-p104">If you attempt to reference a nonexistent field by name, a new **Field** object will be appended to the **Fields** collection with a [Status](status-property-ado-field.md) of **adFieldPendingInsert**. When you call [Update](update-method-ado.md), ADO will create a new field in your data source if allowed by your provider.</span></span>

