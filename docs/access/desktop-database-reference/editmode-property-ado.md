---
title: EditMode プロパティ (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50fe7a1c034e1e60863ee04da523f41bb7eadb46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581407"
---
# <a name="editmode-property-ado"></a>EditMode プロパティ (ADO)


**適用先:** Access 2013、Office 2013

現在のレコードの編集ステータスを示します。

## <a name="return-value"></a>戻り値

[EditModeEnum](editmodeenum.md) 値を返します。

## <a name="remarks"></a>注釈

ADO は、現在のレコードに関連付けられた編集バッファーを保持します。このプロパティは、このバッファーに対して変更が加えられたかどうか、または新しいレコードが作成されたかどうかを示します。現在のレコードの編集状態を調べるには、 **EditMode** プロパティを使います。編集プロセスが中断された場合に保留中の変更があるかどうかを確認して、 [Update](update-method-ado.md) メソッドまたは [CancelUpdate](cancelupdate-method-ado.md) メソッドを使用する必要があるかどうかを判定できます。

さまざまな編集条件における [EditMode](addnew-method-ado.md) プロパティの詳細については、「 **AddNew メソッド (ADO)**」を参照してください。

[Delete](delete-method-ado-recordset.md)の呼び出しでデータ ソース内のレコードまたはレコードが正常に削除されない場合 (参照整合性違反など [)、Recordset](recordset-object-ado.md)は編集モード **(EditMode**  =  **adEditInProgress)** のままです。 これは、(たとえば **Move**、[NextRecordset](move-method-ado.md)、または [Close](nextrecordset-method-ado.md) などを使って) 現在のレコードから移動する前に [CancelUpdate](close-method-ado.md) メソッドを呼び出す必要があることを意味します。


> [!NOTE]
> [!メモ] **EditMode** では現在のレコードがないと有効な値は返されません。 **EditMode** では、 [BOF または EOF](bof-eof-properties-ado.md) が TRUE の場合、または現在のレコードが削除されている場合にエラーが返されます。


