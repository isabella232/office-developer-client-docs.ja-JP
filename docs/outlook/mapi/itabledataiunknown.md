---
title: ITableData IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData
api_type:
- COM
ms.assetid: ac7ae09f-ce19-45cf-8963-fad5bba75452
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 968768fe75286b93bf12e349a4845fdfaa1923e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801232"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**適用対象**: Outlook 
  
テーブルを操作するためのユーティリティ メソッドを提供します。 MAPI には、データ オブジェクトのテーブルまたはテーブルのメンテナンスを実行するサービス プロバイダーのために**ITableData**を実装するオブジェクトが用意されています。 テーブルのデータ オブジェクトを取得するには、サービス プロバイダーは、 [CreateTable](createtable.md)関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって公開されます。  <br/> |テーブルのデータ オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPITableData  <br/> |
|ポインターの型。  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[HrGetView](itabledata-hrgetview.md) <br/> |[IMAPITable](imapitableiunknown.md)実装へのポインターを返す表形式ビューを作成します。  <br/> |
|[HrModifyRow](itabledata-hrmodifyrow.md) <br/> |既存の行が上書きされる、テーブルの新しい行を挿入します。  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |テーブルの行を削除します。  <br/> |
|[HrQueryRow](itabledata-hrqueryrow.md) <br/> |テーブルの行を取得します。  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |テーブル内の位置に基づいて行を取得します。  <br/> |
|[HrNotify](itabledata-hrnotify.md) <br/> |テーブルの行の通知を送信します。  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |テーブルの行を挿入します。  <br/> |
|[HrModifyRows](itabledata-hrmodifyrows.md) <br/> |既存の行が上書きされる、複数のテーブル行を挿入します。  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |複数のテーブル行を削除します。  <br/> |
   
## <a name="remarks"></a>注釈

**ITableData**の MAPI 実装では、非常に大きなテーブルでの使用に適していませんので、メモリ内のすべてのデータと関連付けられている制限を押しながら、テーブルと連携します。 大規模な制限や分類などの複雑な操作はサポートされていません。 
  
テーブルのデータ オブジェクトは、インデックス列、行ごとに一意の値を持つことが保証されているプロパティを使用して行を識別します。 ほとんどのサービス プロバイダーは、インデックス列として**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティを使用します。 複数値を持つプロパティは、インデックス列として使用できません。
  
テーブルのデータ オブジェクトは、変更や削除によって影響を受ける行の数に関係なく 1 つの通知を生成します。 操作の対象の行が存在しない場合は、行が追加されます。
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

