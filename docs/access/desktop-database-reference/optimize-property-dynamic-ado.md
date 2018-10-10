---
title: Optimize プロパティ -- 動的 (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c31950eda813ee4f3f07145d28a83106cf86b3f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477324"
---
# <a name="optimize-property--dynamic-ado"></a><span data-ttu-id="b2ac0-102">Optimize プロパティ -- 動的 (ADO)</span><span class="sxs-lookup"><span data-stu-id="b2ac0-102">Optimize Property--Dynamic (ADO)</span></span>


<span data-ttu-id="b2ac0-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2ac0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b2ac0-104">フィールドにインデックスを作成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="b2ac0-104">Specifies whether an index should be created on a field.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b2ac0-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="b2ac0-105">Settings and Return Values</span></span>

<span data-ttu-id="b2ac0-106">インデックスを作成するかどうかを表すブール型 ( **Boolean** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="b2ac0-106">Sets or returns a **Boolean** value that indicates whether an index should be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2ac0-107">解説</span><span class="sxs-lookup"><span data-stu-id="b2ac0-107">Remarks</span></span>

<span data-ttu-id="b2ac0-p101">インデックスを使用すると、[Recordset](recordset-object-ado.md) の値の検索や並べ替えのパフォーマンスが向上します。インデックスは ADO 内部の機能であり、アプリケーション内で明示的にアクセスしたり使用したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="b2ac0-p101">An index can improve the performance of operations that find or sort values in a [Recordset](recordset-object-ado.md). The index is internal to ADO — you cannot explicitly access or use it in your application.</span></span>

<span data-ttu-id="b2ac0-p102">フィールドにインデックスを作成するには、 **Optimize** プロパティを **True** に設定します。インデックスを削除するには、このプロパティを **False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="b2ac0-p102">To create an index on a field, set the **Optimize** property to **True**. To delete the index, set this property to **False**.</span></span>

<span data-ttu-id="b2ac0-112">**Optimize** は、 [CursorLocation](field-object-ado.md) プロパティが [adUseClient](properties-collection-ado.md) に設定されているときに [Field](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="b2ac0-112">**Optimize** is a dynamic property appended to the [Field](field-object-ado.md) object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

<span data-ttu-id="b2ac0-113">**使用例**</span><span class="sxs-lookup"><span data-stu-id="b2ac0-113">**Usage**</span></span>

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
