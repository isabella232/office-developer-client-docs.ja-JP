---
title: EditMode プロパティ (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293610"
---
# <a name="editmode-property-ado"></a>EditMode プロパティ (ADO)


**適用先:** Access 2013、Office 2013

現在のレコードの編集ステータスを示します。

## <a name="return-value"></a>戻り値

[EditModeEnum](editmodeenum.md) 値を返します。

## <a name="remarks"></a>注釈

ADO は、現在のレコードに関連付けられた編集バッファーを保持します。このプロパティは、このバッファーに対して変更が加えられたかどうか、または新しいレコードが作成されたかどうかを示します。現在のレコードの編集状態を調べるには、 **EditMode** プロパティを使います。編集プロセスが中断された場合に保留中の変更があるかどうかを確認して、 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを使用する必要があるかどうかを判定できます。

さまざまな編集条件における [EditMode](addnew-method-ado.md) プロパティの詳細については、「 **AddNew メソッド (ADO)**」を参照してください。

[削除](delete-method-ado-recordset.md)の呼び出しで、(たとえば、参照整合性違反によって) データソース内の1つまたは複数のレコードが正常に削除されない場合、その[Recordset](recordset-object-ado.md)は編集モードのままになります (**EditMode** = **adEditInProgress**). これは、(たとえば **Move**、[NextRecordset](move-method-ado.md)、または [Close](nextrecordset-method-ado.md) などを使って) 現在のレコードから移動する前に [CancelUpdate](close-method-ado.md) メソッドを呼び出す必要があることを意味します。


> [!NOTE]
> [!メモ] **EditMode** では現在のレコードがないと有効な値は返されません。 **EditMode** では、 [BOF または EOF](bof-eof-properties-ado.md) が TRUE の場合、または現在のレコードが削除されている場合にエラーが返されます。


