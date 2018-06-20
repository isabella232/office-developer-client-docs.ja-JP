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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804094"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**適用されます**: Outlook 
  
何らかの変更やエラーなどのイベントによって影響のあるテーブル内の行について説明します。 テーブル通知が生成されますが発生します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
   
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

**ulTableEvent**
  
> テーブルのイベント タイプを表すために使用するフラグのビットマスクです。 次のフラグを設定することができます。
    
TABLE_CHANGED 
  
> 高いレベルの表について何かが変更されていることを示します。 テーブルの状態は、イベントの前にします。 これは、すべて**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティ、ブックマーク、現在の位置、およびユーザー インターフェイスの選択は、まだ有効であることを意味します。 このイベントを処理するには、テーブルを再読み取り. 豊富なテーブルの通知を実装する必要のないサービス ・ プロバイダーは、特定の種類の変更を示すために詳細なイベントの代わりに TABLE_CHANGED イベントを送信します。 
    
TABLE_ERROR 
  
> 通常、非同期操作の処理中に、エラーが発生しました。 次のメソッドの処理中にエラーは、このイベントを生成できます。 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   TABLE_ERROR イベントを受け取ると、クライアントは、テーブルの内容の正確さに依存できません。 また、保留中の他の変更についての通知は失われます。 最後のメソッド呼び出しからは、以前の時点で作成されたために、 [IMAPITable::GetLastError](imapitable-getlasterror.md)メソッドは、エラーに関する追加情報を提供しない場合があります。 
    
TABLE_RELOAD 
  
> テーブル内のデータを再読み込みする必要があります。 サービス ・ プロバイダーは TABLE_RELOAD を送信すると、たとえば、データベースの基になるデータが格納されているデータベースを交換してください。 何も表がまだ有効であることと仮定すると、テーブルを再読み取りがこのイベントを処理します。 すべてのブックマーク、インスタンスのキー、状態、および位置情報が有効ではありません。
    
TABLE_RESTRICT_DONE 
  
> 制限操作が、 **IMAPITable::Restrict**メソッドの呼び出しで開始したが完了しました。 
    
TABLE_ROW_ADDED 
  
> テーブルと、対応するオブジェクトを保存する新しい行が追加されました。 [IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出した後は、TABLE_ROW_ADDED イベントが生成されます。 
    
TABLE_ROW_DELETED 
  
> テーブルから行が削除されました。 **PropPrior**メンバーは、NULL に設定されています。 
    
TABLE_ROW_MODIFIED 
  
> 行が変更されました。 **行**メンバーには、行の影響を受けるプロパティが含まれています。 複数の TABLE_ROW_MODIFIED イベントは、テーブル ビューに表示される順序で送信されます。 
    
  TABLE_ROW_MODIFIED イベントは、対応するオブジェクトへの変更が、 **IMAPIProp::SaveChanges**メソッドを呼び出して、コミットされた後に送信されます。 ここで変更した行がテーブルの最初の行の場合は、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) は、 **propPrior**メンバーのプロパティ タグの値です。
    
TABLE_SETCOL_DONE 
  
> **IMAPITable::SetColumns**のメソッドの呼び出しを使用して開始列の設定操作が完了しました。 
    
TABLE_SORT_DONE 
  
> テーブルの並べ替えの操作は、 **IMAPITable::SortTable**メソッドの呼び出しで開始したが完了しました。 
    
**hResult**
  
> **UlTableEvent**メンバーは、TABLE_ERROR に設定されている場合、発生したエラーの HRESULT 値です。 
    
**propIndex**
  
> 影響を受ける行の**PR_INSTANCE_KEY**プロパティの値の[SPropValue](spropvalue.md)構造体です。 
    
**propPrior**
  
> 影響を受ける 1 つ前に、の行の**PR_INSTANCE_KEY**プロパティの**SPropValue**構造体です。 影響を受ける行がテーブルの最初の行の場合は、 **PR_NULL**を 0 ではありません**propPrior**を設定しなければなりません。 0 は有効なプロパティのタグではありません。 
    
**row**
  
> [SRow](srow.md)の構造が影響を受ける行を記述します。 この構造体は、テーブルのすべての通知イベントに入力されます。 テーブル通知、イベントの行データを渡さない、**あう**、 **SRow**構造体のメンバーを 0 に設定し、 **lpProps**メンバーは NULL に設定します。 この**SRow**の構造が読み取り専用であるためクライアントは、変更を加える必要がある場合のコピーを行う必要があります。 コピーを作成するのには、 [ScDupPropset](scduppropset.md)関数を使用できます。 
    
## <a name="remarks"></a>備考

**テーブル\_通知**構造体は、[通知](notification.md)の構造体のメンバー**情報**に含まれる構造体の共用体のメンバーの 1 つです。 **情報**メンバーが含まれています、**テーブル\_通知**、 **ulEventType**構造体のメンバーが_fnevTableModified_に設定されている場合を構造化します。
  
行メンバーの列の型と順序は、順序と、通知が生成された時点で有効であったタイプを反映します。 順序と種類の通知が生成された時点では必ずしもと同じ通知が配布されたときです。 
  
通知の詳細については、次の表に記載されているトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI でのイベントの通知](event-notification-in-mapi.md) <br/> |通知と通知のイベントの概要です。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[イベント通知をサポートしています。](supporting-event-notification.md) <br/> |サービス プロバイダーが、 **IMAPISupport**メソッドを使用して、通知を生成する方法について説明します。  <br/> |
   
テーブルの通知は非同期であるために、クライアントは別の方法で追加について学習した後、追加された行の通知を受信できます。 **IMAPITable::Sort**、 **IMAPITable::Restrict**、または**IMAPITable::SetColumns**メソッドでエラーが表示されるか、プロセスで、テーブルを更新しようとした、基になるときは、TABLE_ERROR イベントを受信することはまたは行を変更します。 
  
## <a name="see-also"></a>関連項目

- [�ʒm](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI の構造](mapi-structures.md)

