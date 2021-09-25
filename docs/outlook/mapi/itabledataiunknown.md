---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ac60e3691f64ab932f7d8a53370f43efaa0fa9ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571564"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルを操作するユーティリティ メソッドを提供します。 MAPI には、サービス プロバイダーがテーブルのメンテナンスを実行するのに役立つ **、ITableData** を実装するテーブル データ オブジェクトまたはオブジェクトが提供されています。 テーブル データ オブジェクトを取得するために、サービス プロバイダーは [CreateTable 関数を呼び出](createtable.md) します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|次のユーザーによって公開されます。  <br/> |テーブル データ オブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPITableData  <br/> |
|ポインターの種類:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |IMAPITable 実装へのポインターを返すテーブル [ビューを作成](imapitableiunknown.md) します。  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |新しいテーブル行を挿入し、既存の行を置き換える可能性があります。  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |テーブル行を削除します。  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |テーブル行を取得します。  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |テーブル内の位置に基づいて行を取得します。  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |テーブル行の通知を送信します。  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |テーブル行を挿入します。  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |複数のテーブル行を挿入し、既存の行を置き換える可能性があります。  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |複数のテーブル行を削除します。  <br/> |
   
## <a name="remarks"></a>注釈

**ITableData** の MAPI 実装は、すべてのデータと関連する制限をメモリに保持することでテーブルと動作し、非常に大きなテーブルでの使用には適しなされません。 大きな制限や、分類などの複雑な操作はサポートされていません。 
  
テーブル データ オブジェクトは、各行に一意の値を持つプロパティであるインデックス列を使用して行を識別します。 ほとんどのサービス プロバイダーは **、PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティをインデックス列として使用します。 複数の値を持つプロパティをインデックス列として使用することはできません。
  
テーブル データ オブジェクトは、変更または削除の影響を受ける行の数に関係なく、1 つの通知を生成します。 操作のターゲット行が存在しない場合は、行が追加されます。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

