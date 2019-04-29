---
title: itabledata IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3992bea899239ee5975505dec366490d6bbe1698
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430596"
---
# <a name="itabledata--iunknown"></a>ITableData : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルを処理するためのユーティリティメソッドを提供します。 MAPI は、サービスプロバイダーがテーブルのメンテナンスを実行するのに役立つ、 **itabledata**を実装するテーブルデータオブジェクトまたはオブジェクトを提供します。 テーブルデータオブジェクトを取得するために、サービスプロバイダーは[CreateTable](createtable.md)関数を呼び出します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|公開者:  <br/> |テーブルデータオブジェクト  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPITableData  <br/> |
|ポインターの種類:  <br/> |LPTABLEDATA  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[hrgetview](itabledata-hrgetview.md) <br/> |[IMAPITable](imapitableiunknown.md)実装へのポインターを返すテーブルビューを作成します。  <br/> |
|[hrmodifyrow](itabledata-hrmodifyrow.md) <br/> |既存の行を置き換える可能性がある新しいテーブル行を挿入します。  <br/> |
|[HrDeleteRow](itabledata-hrdeleterow.md) <br/> |表の行を削除します。  <br/> |
|[hrqueryrow](itabledata-hrqueryrow.md) <br/> |表の行を取得します。  <br/> |
|[HrEnumRow](itabledata-hrenumrow.md) <br/> |テーブル内の位置に基づいて行を取得します。  <br/> |
|[hrnotify](itabledata-hrnotify.md) <br/> |表の行の通知を送信します。  <br/> |
|[HrInsertRow](itabledata-hrinsertrow.md) <br/> |表の行を挿入します。  <br/> |
|[hrmodifyrows](itabledata-hrmodifyrows.md) <br/> |複数のテーブル行を挿入します。既存の行を置換する場合もあります。  <br/> |
|[HrDeleteRows](itabledata-hrdeleterows.md) <br/> |複数の表の行を削除します。  <br/> |
   
## <a name="remarks"></a>注釈

**itabledata**の MAPI 実装は、すべてのデータと、関連するすべての制限をメモリに保持することによってテーブルで機能し、非常に大きなテーブルで使用するのに適していません。 大規模な制限や分類などの複雑な操作はサポートされていません。 
  
テーブルデータオブジェクトは、インデックス列を使用して行を識別します。プロパティは、各行に一意の値があることが保証されます。 ほとんどのサービスプロバイダーは、インデックス列として**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティを使用します。 複数の値を持つプロパティをインデックス列として使用することはできません。
  
テーブルデータオブジェクトは、変更または削除によって影響を受ける行の数に関係なく、1つの通知を生成します。 操作の対象となる行が存在しない場合は、行が追加されます。
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

