---
title: unique Table、unique Schema、unique Catalog 動的プロパティ (ADO)
TOCTitle: Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)
ms:assetid: e6374782-755b-322b-21de-6d6a386dcd98
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250169(v=office.15)
ms:contentKeyID: 48548374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5f4bf93afc200edd88e89cf5d4e90435c2476942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32313749"
---
# <a name="unique-table-unique-schema-unique-catalog-dynamic-properties-ado"></a><span data-ttu-id="c4da7-102">unique Table、unique Schema、unique Catalog 動的プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="c4da7-102">Unique Table, Unique Schema, Unique Catalog dynamic properties (ADO)</span></span>


<span data-ttu-id="c4da7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4da7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4da7-104">複数のベース テーブルに対する JOIN 操作で形成された [Recordset](recordset-object-ado.md) 中の、特定のベース テーブルに対する変更を細かく制御します。</span><span class="sxs-lookup"><span data-stu-id="c4da7-104">Enables you to closely control modifications to a particular base table in a [Recordset](recordset-object-ado.md) that was formed by a JOIN operation on multiple base tables.</span></span>

  - <span data-ttu-id="c4da7-105">**Unique Table** は、更新、挿入、および削除の操作ができるベース テーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4da7-105">**Unique Table** specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span>

  - <span data-ttu-id="c4da7-106">**Unique schema**は、*スキーマ*、またはテーブルの所有者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4da7-106">**Unique Schema** specifies the *schema*, or name of the owner of the table.</span></span>

  - <span data-ttu-id="c4da7-107">**Unique catalog**は、*カタログ*、またはテーブルを含むデータベースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4da7-107">**Unique Catalog** specifies the *catalog*, or name of the database containing the table.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c4da7-108">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="c4da7-108">Settings and return values</span></span>

<span data-ttu-id="c4da7-109">テーブル、スキーマ、またはカタログの名前である文字列型 (**String**) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="c4da7-109">Sets or returns a **String** value that is the name of a table, schema, or catalog.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4da7-110">注釈</span><span class="sxs-lookup"><span data-stu-id="c4da7-110">Remarks</span></span>

<span data-ttu-id="c4da7-p101">対象となるベース テーブルは、一意なカタログ名、スキーマ名、およびテーブル名で識別します。 **Unique Table** プロパティが設定されている場合、 **Unique Schema** プロパティまたは **Unique Catalog** プロパティの値がベース テーブルを検索するために使用されます。 **Unique Table** プロパティを設定する前に **Unique Schema** プロパティと **Unique Catalog** プロパティのどちらかまたは両方を設定するのが本来の順序ですが、必ずしもそうする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c4da7-p101">The desired base table is uniquely identified by its catalog, schema, and table names. When the **Unique Table** property is set, the values of the **Unique Schema** or **Unique Catalog** properties are used to find the base table. It is intended, but not required, that either or both the **Unique Schema** and **Unique Catalog** properties be set before the **Unique Table** property is set.</span></span>

<span data-ttu-id="c4da7-p102">**Unique Table** の主キーは、 **Recordset** 全体の主キーとして扱われます。これは、主キーを必要とするすべてのメソッドで使用されるキーです。</span><span class="sxs-lookup"><span data-stu-id="c4da7-p102">The primary key of the **Unique Table** is treated as the primary key of the entire **Recordset**. This is the key that is used for any method requiring a primary key.</span></span>

<span data-ttu-id="c4da7-p103">**Unique Table** が設定されている場合、 [Delete](delete-method-ado-recordset.md) メソッドは、指定されたテーブルだけに反映されます。 [AddNew](addnew-method-ado.md) メソッド、 [Resync](resync-method-ado.md) メソッド、 [Update](update-method-ado.md) メソッド、および [UpdateBatch](updatebatch-method-ado.md) メソッドは、 **Recordset** の基になるベース テーブルに反映されます。</span><span class="sxs-lookup"><span data-stu-id="c4da7-p103">While **Unique Table** is set, the [Delete](delete-method-ado-recordset.md) method affects only the named table. The [AddNew](addnew-method-ado.md), [Resync](resync-method-ado.md), [Update](update-method-ado.md), and [UpdateBatch](updatebatch-method-ado.md) methods affect any appropriate underlying base tables of the **Recordset**.</span></span>

<span data-ttu-id="c4da7-p104">カスタム再同期を実行するには、あらかじめ **Unique Table** を指定する必要があります。 **Unique Table** が指定されていないと、 [Resync Command](resync-command-property-dynamic-ado.md) プロパティは反映されません。</span><span class="sxs-lookup"><span data-stu-id="c4da7-p104">**Unique Table** must be specified before doing any custom resynchronizations. If **Unique Table** has not been specified, the [Resync Command](resync-command-property-dynamic-ado.md) property will have no effect.</span></span>

<span data-ttu-id="c4da7-120">一意のベース テーブルが見つからないと、実行時エラーになります。</span><span class="sxs-lookup"><span data-stu-id="c4da7-120">A run-time error results if a unique base table cannot be found.</span></span>

<span data-ttu-id="c4da7-121">**CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定すると、これらの動的プロパティは、すべてその [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="c4da7-121">These dynamic properties are all appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

