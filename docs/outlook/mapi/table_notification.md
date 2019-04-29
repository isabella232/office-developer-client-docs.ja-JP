---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415958"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**適用対象**: Outlook 2013 | Outlook 2016 
  
変更やエラーなど、何らかの種類のイベントの影響を受けたテーブル内の行について説明します。 これにより、テーブル通知が生成されます。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a>メンバー

**ultableevent**
  
> テーブルイベントの種類を表すために使用されるフラグのビットマスク。 次のフラグを設定できます。
    
TABLE_CHANGED 
  
> テーブルに関する何らかの変更が、高レベルであることを示します。 テーブルの状態はイベントの前と同じです。 これは、すべての**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ、ブックマーク、現在の配置、およびユーザーインターフェイスの選択が有効なままであることを意味します。 このイベントを処理するには、テーブルを再度読み込みます。 リッチテーブル通知を実装しないサービスプロバイダーは、より詳細なイベントの代わりに TABLE_CHANGED イベントを送信して、特定の種類の変更を示します。 
    
TABLE_ERROR 
  
> エラーが発生しました。通常は、非同期操作の処理中です。 次のメソッドの処理中にエラーが発生すると、このイベントが発生する可能性があります。 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   TABLE_ERROR イベントを受け取った後、クライアントはテーブルの内容の正確性を信頼できません。 また、他の変更に関する保留中の通知が失われる可能性があります。 [IMAPITable:: GetLastError](imapitable-getlasterror.md)メソッドは、前の時点で生成されたものではなく、最後のメソッドの呼び出しからは、エラーに関する追加情報を提供していない場合があります。 
    
TABLE_RELOAD 
  
> テーブル内のデータを再度読み込む必要があります。 サービスプロバイダーは、たとえば、基になるデータがデータベースに格納され、データベースが置換されるときに、TABLE_RELOAD を送信します。 このイベントを処理するのは、テーブルに関する情報がまだ有効でないことを前提にして、テーブルを再度読み込みます。 すべてのブックマーク、インスタンスキー、状態、および配置情報が無効です。
    
TABLE_RESTRICT_DONE 
  
> **IMAPITable:: Restrict**メソッド呼び出しで開始された制限の操作が完了しました。 
    
TABLE_ROW_ADDED 
  
> テーブルに新しい行が追加され、対応するオブジェクトが保存されます。 TABLE_ROW_ADDED イベントは、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後に生成されます。 
    
TABLE_ROW_DELETED 
  
> 行がテーブルから削除されました。 **propprior**メンバーは NULL に設定されています。 
    
TABLE_ROW_MODIFIED 
  
> 行が変更されました。 行**** メンバーには、行の影響を受けるプロパティが含まれています。 複数の TABLE_ROW_MODIFIED イベントは、テーブルビューに表示される順序で送信されます。 
    
  TABLE_ROW_MODIFIED イベントは、対応するオブジェクトへの変更が、 **imapiprop:: SaveChanges**メソッドへの呼び出しを使用してコミットされた後に送信されます。 変更された行がテーブルの最初の行になった場合、その**前**のメンバーのプロパティタグの値は**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) になります。
    
TABLE_SETCOL_DONE 
  
> **IMAPITable:: SetColumns**メソッド呼び出しで開始された列設定操作が完了しました。 
    
TABLE_SORT_DONE 
  
> **IMAPITable:: sorttable**メソッド呼び出しで開始されたテーブルの並べ替え操作が完了しました。 
    
**hResult**
  
> **ultableevent**メンバーが TABLE_ERROR に設定されている場合に、発生したエラーの HRESULT 値。 
    
**propindex**
  
> 影響を受ける行の**PR_INSTANCE_KEY**プロパティの[spropvalue](spropvalue.md)構造。 
    
**propprior**
  
> 影響を受ける前の行の**PR_INSTANCE_KEY**プロパティの**spropvalue**構造。 影響を受ける行がテーブルの最初の行である**** 場合は、 **PR_NULL**を0以外の値に設定する必要があります。 0は、有効なプロパティタグではありません。 
    
**row**
  
> 影響を受ける行を説明する[srow](srow.md)構造。 この構造体は、すべてのテーブル通知イベントに対して入力されます。 行データを渡さないテーブル通知イベントの場合、 **srow**構造の**cvalues**メンバーは0に設定され、 **lpprops**メンバーは NULL に設定されます。 この**srow**構造は読み取り専用であるためです。クライアントは、変更を行う場合は、そのコピーを作成する必要があります。 [ScDupPropset](scduppropset.md)関数を使用してコピーを作成できます。 
    
## <a name="remarks"></a>注釈

**表\_通知**構造は、[通知](notification.md)構造の**info**メンバに含まれている構造体の和集合のメンバーのいずれかです。 構造体の**uleventtype**メンバーが_fnevTableModified_に設定されている場合、 **info**メンバーには**テーブル\_通知**構造が含まれています。
  
行メンバーの列の順序と種類は、通知が生成されたときに有効だった順序と種類を反映しています。 通知が生成されたときの順序と種類は、通知が配信されたときと必ずしも同じではありません。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法についての説明。  <br/> |
|[イベント通知のサポート](supporting-event-notification.md) <br/> |サービスプロバイダーが**imapisupport**メソッドを使用して通知を生成する方法についての説明。  <br/> |
   
テーブル通知は非同期であるため、クライアントは別の方法で追加について学習した後に、追加された行の通知を受け取ることができます。 TABLE_ERROR イベントは、 **IMAPITable:: Sort**、 **IMAPITable:: Restrict**、または**IMAPITable:: SetColumns**メソッドでエラーが発生した場合、または基になるプロセスがテーブルを更新しようとした場合 (たとえば、new または変更された行 
  
## <a name="see-also"></a>関連項目

- [�ʒm](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI の構造](mapi-structures.md)

