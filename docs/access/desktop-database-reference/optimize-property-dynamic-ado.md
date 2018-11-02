---
title: Optimize 動的プロパティ (ADO)
TOCTitle: Optimize dynamic property (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a1fff5911080811bc2556a20667ff2f2391f22e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926781"
---
# <a name="optimize-dynamic-property-ado"></a><span data-ttu-id="c0f84-102">Optimize 動的プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c0f84-102">Optimize dynamic property (ADO)</span></span>


<span data-ttu-id="c0f84-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c0f84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c0f84-104">フィールドにインデックスを作成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c0f84-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c0f84-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="c0f84-105">Settings and return values</span></span>

<span data-ttu-id="c0f84-106">インデックスを作成するかどうかを表すブール型 ( **Boolean** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c0f84-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f84-107">解説</span><span class="sxs-lookup"><span data-stu-id="c0f84-107">Remarks</span></span>

<span data-ttu-id="c0f84-p101">インデックスを使用すると、[Recordset](recordset-object-ado.md) の値の検索や並べ替えのパフォーマンスが向上します。インデックスは ADO 内部の機能であり、アプリケーション内で明示的にアクセスしたり使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c0f84-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="c0f84-p102">フィールドにインデックスを作成するには、 **Optimize** プロパティを **True** に設定します。インデックスを削除するには、このプロパティを **False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c0f84-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="c0f84-112">**Optimize** は、 [CursorLocation](field-object-ado.md) プロパティが [adUseClient](properties-collection-ado.md) に設定されているときに [Field](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="c0f84-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="c0f84-113">**使用例**</span><span class="sxs-lookup"><span data-stu-id="c0f84-113">**Usage**</span></span>

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
