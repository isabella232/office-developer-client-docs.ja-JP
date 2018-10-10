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
# <a name="editmode-property-ado"></a>EditMode プロパティ (ADO)


**適用されます**Access 2013 |。Office 2013

現在のレコードの編集ステータスを示します。

## <a name="return-value"></a>戻り値

[EditModeEnum](editmodeenum.md) 値を返します。

## <a name="remarks"></a>解説

ADO は、現在のレコードに関連付けられた編集バッファーを保持します。このプロパティは、このバッファーに対して変更が加えられたかどうか、または新しいレコードが作成されたかどうかを示します。現在のレコードの編集状態を調べるには、 **EditMode** プロパティを使います。編集プロセスが中断された場合に保留中の変更があるかどうかを確認して、 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを使用する必要があるかどうかを判定できます。

さまざまな編集条件における [EditMode](addnew-method-ado.md) プロパティの詳細については、「 **AddNew メソッド (ADO)**」を参照してください。

[削除](delete-method-ado-recordset.md)する呼び出しが正常にレコードは削除、またはデータのレコードでは、[レコード セット](recordset-object-ado.md)を (参照整合性違反など) のためにソースと編集モードのまま (**EditMode** = **adEditInProgress**). これは、(たとえば **Move**、[NextRecordset](move-method-ado.md)、または [Close](nextrecordset-method-ado.md) などを使って) 現在のレコードから移動する前に [CancelUpdate](close-method-ado.md) メソッドを呼び出す必要があることを意味します。


> [!NOTE]
> <P>[!メモ] <STRONG>EditMode</STRONG> では現在のレコードがないと有効な値は返されません。 <STRONG>EditMode</STRONG> では、 <A href="bof-eof-properties-ado.md">BOF または EOF</A> が TRUE の場合、または現在のレコードが削除されている場合にエラーが返されます。</P>


