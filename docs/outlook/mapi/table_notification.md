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
# <a name="table_notification"></a>TABLE_NOTIFICATION

**適用対象**: Outlook 2013 | Outlook 2016 
  
変更やエラーなど、何らかの種類のイベントの影響を受けたテーブル内の行について説明します。 これにより、テーブル通知が生成されます。 
  
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

## <a name="members"></a>Members

**ulTableEvent**
  
> テーブル イベントの種類を表すフラグのビットマスク。 次のフラグを設定できます。
    
TABLE_CHANGED 
  
> テーブルに関する情報が変更されたことを高レベルで示します。 テーブルの状態は、イベントの前の状態です。 つまり **、すべてのPR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティ、ブックマーク、現在の配置、およびユーザー インターフェイスの選択は引き続き有効です。 テーブルを再読み込みして、このイベントを処理します。 リッチ テーブル通知を実装しないサービス プロバイダーは、特定の種類の変更TABLE_CHANGED詳細なイベントではなく、イベントを送信します。 
    
TABLE_ERROR 
  
> 通常、非同期操作の処理中にエラーが発生しました。 次のメソッドの処理中にエラーが発生すると、このイベントが発生する可能性があります。 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   イベントを受信TABLE_ERROR、クライアントは表の内容の精度に依存できません。 また、他の変更に関する保留中の通知が失われる可能性があります。 [IMAPITable::GetLastError](imapitable-getlasterror.md)メソッドは、以前の時点で生成されたエラーに関する追加情報を提供しない場合があります。必ずしも最後のメソッド呼び出しから生成されたとは限りません。 
    
TABLE_RELOAD 
  
> テーブル内のデータを再読み込みする必要があります。 サービス プロバイダーは、TABLE_RELOAD基になるデータがデータベースに格納され、データベースが置き換えられた場合に、このデータを送信します。 テーブルに関する何も有効でないと仮定し、テーブルを再読み込みすることで、このイベントを処理します。 ブックマーク、インスタンス キー、状態、および位置情報はすべて無効です。
    
TABLE_RESTRICT_DONE 
  
> **IMAPITable::Restrict** メソッド呼び出しで開始された制限操作が完了しました。 
    
TABLE_ROW_ADDED 
  
> テーブルに新しい行が追加され、対応するオブジェクトが保存されました。 TABLE_ROW_ADDEDは [、IMAPIProp::SaveChanges](imapiprop-savechanges.md) メソッドの呼び出し後に生成されます。 
    
TABLE_ROW_DELETED 
  
> テーブルから行が削除されました。 **propPrior メンバーは** NULL に設定されます。 
    
TABLE_ROW_MODIFIED 
  
> 行が変更されました。 行 **メンバーには** 、その行の影響を受けるプロパティが含まれる。 複数TABLE_ROW_MODIFIEDイベントは、テーブル ビューに表示される順序で送信されます。 
    
  TABLE_ROW_MODIFIEDは **、IMAPIProp::SaveChanges** メソッドの呼び出しで、対応するオブジェクトに対する変更がコミットされた後に送信されます。 変更された行がテーブルの最初の行である場合 **、propPrior** メンバーのプロパティ タグの値は PR_NULL ([PidTagNull) になります](pidtagnull-canonical-property.md)。 
    
TABLE_SETCOL_DONE 
  
> **IMAPITable::SetColumns** メソッド呼び出しで開始された列設定操作が完了しました。 
    
TABLE_SORT_DONE 
  
> **IMAPITable::SortTable** メソッド呼び出しで開始されたテーブルの並べ替え操作が完了しました。 
    
**hResult**
  
> ulTableEvent メンバーがエラーに設定されている場合に発生したエラーの **HRESULT** TABLE_ERROR。 
    
**propIndex**
  
> [影響を受](spropvalue.md) ける **行の** PR_INSTANCE_KEYプロパティの SPropValue 構造体。 
    
**propPrior**
  
> **影響を受** ける行の **前PR_INSTANCE_KEY** プロパティの SPropValue 構造体。 影響を受ける行が表の最初の行である場合 **、propPrior** は 0 ではなく、PR_NULL **に設定** する必要があります。 ゼロは有効なプロパティ タグではありません。 
    
**row**
  
> [影響を受](srow.md) ける行を記述する SRow 構造体。 この構造は、すべてのテーブル通知イベントに対して入力されます。 行データを渡していないテーブル通知イベントの場合 **、SRow** 構造体の **cValues** メンバーは 0 に設定され **、lpProps** メンバーは NULL に設定されます。 この **SRow 構造体は** 読み取り専用のためです。クライアントが変更を行う場合は、そのコピーを作成する必要があります。 [ScDupPropset 関数](scduppropset.md)を使用してコピーを作成できます。 
    
## <a name="remarks"></a>注釈

**TABLE \_ NOTIFICATION 構造体** は、NOTIFICATION 構造体の info メンバーに含まれる構造体の共用体のメンバーの [1](notification.md)つです。  info **メンバー** には、構造体の **ulEventType** メンバーが _fnevTableModified_ に設定されている場合に TABLE NOTIFICATION 構造が含まれます。 **\_**
  
行メンバーの列の順序と種類は、通知が生成された時点で有効だった順序と種類を反映します。 通知が生成された時点での順序と種類は、通知が配信された場合と必ずしも同じではありません。 
  
通知の詳細については、次の表で説明するトピックを参照してください。
  
|**トピック**|**説明**|
|:-----|:-----|
|[MAPI のイベント通知](event-notification-in-mapi.md) <br/> |通知イベントと通知イベントの一般的な概要。  <br/> |
|[通知の処理](handling-notifications.md) <br/> |クライアントが通知を処理する方法について説明します。  <br/> |
|[サポート イベント通知](supporting-event-notification.md) <br/> |サービス プロバイダーが **IMAPISupport** メソッドを使用して通知を生成する方法について説明します。  <br/> |
   
テーブル通知は非同期なので、クライアントは別の方法で追加について学習した後、追加された行の通知を受け取ります。 **IMAPITable::Sort** **、IMAPITable::Restrict、または** **IMAPITable::SetColumns** メソッドでエラーが発生した場合、または基になるプロセスが新しい行や変更された行を含むテーブルを更新しようとすると、TABLE_ERROR イベントを受け取る可能性があります。 
  
## <a name="see-also"></a>関連項目

- [�ʒm](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [MAPI の構造](mapi-structures.md)

