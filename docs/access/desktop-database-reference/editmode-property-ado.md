---
title: EditMode プロパティ (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476915"
---
# <a name="editmode-property-ado"></a><span data-ttu-id="e18c7-102">EditMode プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e18c7-102">EditMode Property (ADO)</span></span>


<span data-ttu-id="e18c7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e18c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e18c7-104">現在のレコードの編集ステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e18c7-104">Indicates the editing status of the current record.</span></span>

## <a name="return-value"></a><span data-ttu-id="e18c7-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="e18c7-105">Return Value</span></span>

<span data-ttu-id="e18c7-106">[EditModeEnum](editmodeenum.md) 値を返します。</span><span class="sxs-lookup"><span data-stu-id="e18c7-106">Returns an [EditModeEnum](editmodeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e18c7-107">解説</span><span class="sxs-lookup"><span data-stu-id="e18c7-107">Remarks</span></span>

<span data-ttu-id="e18c7-p101">ADO は、現在のレコードに関連付けられた編集バッファーを保持します。このプロパティは、このバッファーに対して変更が加えられたかどうか、または新しいレコードが作成されたかどうかを示します。現在のレコードの編集状態を調べるには、 **EditMode** プロパティを使います。編集プロセスが中断された場合に保留中の変更があるかどうかを確認して、 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを使用する必要があるかどうかを判定できます。</span><span class="sxs-lookup"><span data-stu-id="e18c7-p101">ADO maintains an editing buffer associated with the current record. This property indicates whether changes have been made to this buffer, or whether a new record has been created. Use the **EditMode** property to determine the editing status of the current record. You can test for pending changes if an editing process has been interrupted and determine whether you need to use the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method.</span></span>

<span data-ttu-id="e18c7-112">さまざまな編集条件における [EditMode](addnew-method-ado.md) プロパティの詳細については、「 **AddNew メソッド (ADO)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e18c7-112">See the [AddNew](addnew-method-ado.md) method for a more detailed description of the **EditMode** property under different editing conditions.</span></span>

<span data-ttu-id="e18c7-113">[削除](delete-method-ado-recordset.md)する呼び出しが正常にレコードは削除、またはデータのレコードでは、[レコード セット](recordset-object-ado.md)を (参照整合性違反など) のためにソースと編集モードのまま (**EditMode** = **adEditInProgress**).</span><span class="sxs-lookup"><span data-stu-id="e18c7-113">When a call to [Delete](delete-method-ado-recordset.md) does not successfully delete the record or records in the data source (due to referential integrity violations, for example), the [Recordset](recordset-object-ado.md) will remain in edit mode (**EditMode** = **adEditInProgress**).</span></span> <span data-ttu-id="e18c7-114">これは、(たとえば **Move**、[NextRecordset](move-method-ado.md)、または [Close](nextrecordset-method-ado.md) などを使って) 現在のレコードから移動する前に [CancelUpdate](close-method-ado.md) メソッドを呼び出す必要があることを意味します。</span><span class="sxs-lookup"><span data-stu-id="e18c7-114">This means that **CancelUpdate** must be called before moving off the current record (with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md), for example).</span></span>


> [!NOTE]
> <P><span data-ttu-id="e18c7-p103">[!メモ] <STRONG>EditMode</STRONG> では現在のレコードがないと有効な値は返されません。 <STRONG>EditMode</STRONG> では、 <A href="bof-eof-properties-ado.md">BOF または EOF</A> が TRUE の場合、または現在のレコードが削除されている場合にエラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="e18c7-p103"><STRONG>EditMode</STRONG> can return a valid value only if there is a current record. <STRONG>EditMode</STRONG> will return an error if <A href="bof-eof-properties-ado.md">BOF or EOF</A> is true, or if the current record has been deleted.</span></span></P>


