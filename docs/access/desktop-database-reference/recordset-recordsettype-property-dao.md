---
title: RecordsetType プロパティ (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307631"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="cd4d7-102">RecordsetType プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd4d7-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="cd4d7-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd4d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd4d7-p101">"**RecordsetType**/レコードセット" プロパティを使用すると、フォームで編集可能なレコードセットの種類を指定できます。値の取得および設定が可能です。バイト型 (**Byte**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4d7-106">構文</span><span class="sxs-lookup"><span data-stu-id="cd4d7-106">Syntax</span></span>

<span data-ttu-id="cd4d7-107">*式*。RecordsetType</span><span class="sxs-lookup"><span data-stu-id="cd4d7-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="cd4d7-108">*式*: **Form** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd4d7-109">注釈</span><span class="sxs-lookup"><span data-stu-id="cd4d7-109">Remarks</span></span>

<span data-ttu-id="cd4d7-110">Microsoft Office Access データベースでは、"**RecordsetType**/レコードセット" プロパティの設定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd4d7-111">Setting</span><span class="sxs-lookup"><span data-stu-id="cd4d7-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="cd4d7-112">レコードセットの種類</span><span class="sxs-lookup"><span data-stu-id="cd4d7-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="cd4d7-113">説明</span><span class="sxs-lookup"><span data-stu-id="cd4d7-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd4d7-114">.0</span><span class="sxs-lookup"><span data-stu-id="cd4d7-114">0</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-115">ダイナセットタイプ</span><span class="sxs-lookup"><span data-stu-id="cd4d7-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-116">限り1対1のリレーションシップを持つ単一のテーブルに基づいて、連結コントロールを編集できます。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="cd4d7-117">一対多リレーションシップが設定されたテーブルに基づいてフィールドに連結されたコントロールの場合、テーブル間で連鎖更新&quot;が&quot;有効になっていない限り、リレーションシップの一方の結合フィールドのデータを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd4d7-118">1-d</span><span class="sxs-lookup"><span data-stu-id="cd4d7-118">1</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-119">Dynaset (Inconsistent Updates)/ダイナセット (矛盾を許す)</span><span class="sxs-lookup"><span data-stu-id="cd4d7-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-120">フィールドに連結されたすべてのテーブルとコントロールを編集できます。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd4d7-121">pbm-2</span><span class="sxs-lookup"><span data-stu-id="cd4d7-121">2</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-122">スナップショット</span><span class="sxs-lookup"><span data-stu-id="cd4d7-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-123">フィールドに連結されたテーブルまたはコントロールは編集できません。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cd4d7-124">[!メモ] フォームをフォーム ビューまたはデータシート ビューで表示しているときに、連結コントロール内のデータを編集できないようにするには、" **RecordsetType**/レコードセット" プロパティを 2 に設定します。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="cd4d7-125">Microsoft Office Access プロジェクト (.adp) では、" **RecordsetType**/レコードセット" プロパティの設定値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd4d7-126">Setting</span><span class="sxs-lookup"><span data-stu-id="cd4d7-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="cd4d7-127">レコードセットの種類</span><span class="sxs-lookup"><span data-stu-id="cd4d7-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="cd4d7-128">説明</span><span class="sxs-lookup"><span data-stu-id="cd4d7-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd4d7-129">1/3</span><span class="sxs-lookup"><span data-stu-id="cd4d7-129">3</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-130">スナップショット</span><span class="sxs-lookup"><span data-stu-id="cd4d7-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-131">フィールドに連結されたテーブルまたはコントロールは編集できません。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd4d7-132">2/4</span><span class="sxs-lookup"><span data-stu-id="cd4d7-132">4</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-133">Updatable Snapshot/更新可能なスナップショット</span><span class="sxs-lookup"><span data-stu-id="cd4d7-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="cd4d7-134">フィールドに連結されたすべてのテーブルとコントロールを編集できます。(既定値)</span><span class="sxs-lookup"><span data-stu-id="cd4d7-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cd4d7-135">[!メモ] 開いているフォームまたはレポートの " **RecordsetType**/レコードセット" プロパティを変更すると、自動的にレコードセットが再作成されます。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="cd4d7-p103">複数のテーブルを基にフォームを作成し、コントロールをフィールドと連結させることができます。" **RecordsetType**/レコードセット" プロパティの設定値によって、どのコントロールを編集可能にするかを制限できます。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="cd4d7-p104">"**RecordsetType**/レコードセット" プロパティによって提供される編集の制御機能のほかに、フォームの各コントロールには "**Locked**/編集ロック" プロパティがあります。このプロパティを使うと、コントロールとその基になるデータを編集できるかどうかを指定できます。"**Locked**/編集ロック" プロパティが [Yes/はい] に設定されている場合は、データを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-p104">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited. If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="cd4d7-140">例</span><span class="sxs-lookup"><span data-stu-id="cd4d7-140">Example</span></span>

<span data-ttu-id="cd4d7-p105">次の使用例では、ユーザー ID が ADMIN の場合にだけ、レコードを更新できます。ここでは、パブリック変数 gstrUserID の値が ADMIN でない場合、"**RecordsetType**/レコードセット" プロパティを [Snapshot/スナップショット] に設定します。</span><span class="sxs-lookup"><span data-stu-id="cd4d7-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="cd4d7-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd4d7-143">See also</span></span>

- [<span data-ttu-id="cd4d7-144">Form オブジェクト</span><span class="sxs-lookup"><span data-stu-id="cd4d7-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


