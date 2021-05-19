---
title: PidTagMessageStatus 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355721"
---
# <a name="pidtagmessagestatus-canonical-property"></a>PidTagMessageStatus 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
コンテンツ テーブル内のメッセージの状態を定義するフラグの 32 ビット ビットマスクが含まれる。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MSG_STATUS  <br/> |
|識別子:  <br/> |0x0E17  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>注釈

メッセージは、コンテンツ テーブルと 1 つ以上の検索結果テーブルに存在し、メッセージの各インスタンスの状態が異なる場合があります。 このプロパティは、メッセージのプロパティではなく、コンテンツ テーブル内の列と見なす必要があります。 
  
クライアント アプリケーションは、このプロパティで次の 1 つ以上のフラグを設定できます。 
  
MSGSTATUS_ANSWERED 
  
> メッセージが返信されました。 
    
MSGSTATUS_DELMARKED 
  
> メッセージは、後続の削除のマークが付けされています。 
    
MSGSTATUS_DRAFT 
  
> メッセージが下書きリビジョンの状態です。 
    
MSGSTATUS_HIDDEN 
  
> メッセージは受信者のフォルダー表示から抑制されます。 
    
MSGSTATUS_HIGHLIGHTED 
  
> メッセージは受信者のフォルダー表示で強調表示されます。 
    
MSGSTATUS_REMOTE_DELETE 
  
> メッセージは、ローカル クライアントにダウンロードせずにリモート メッセージ ストアで削除のマークが付けされています。 
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> メッセージは、リモート メッセージ ストアからローカル クライアントにダウンロードするマークが付けされています。 
    
MSGSTATUS_TAGGED 
  
> メッセージは、クライアント定義の目的でタグ付けされています。
    
クライアントMSGSTATUS_DELMARKED、MSGSTATUS_HIDDEN、MSGSTATUS_HIGHLIGHTED、MSGSTATUS_TAGGED **フラグが** 定義されます。  トランスポートプロバイダーとストア プロバイダーは、アクションなしでこれらのビットを渡します。 
  
クライアントは、アプリケーションに適した方法でこれらの値を解釈できます。 多くのクライアントでこのプロパティを使用する方法の 1 つは、削除のマークが付いたメッセージを代表的なアイコンで表示する方法です。 
  
リモート ビューアー クライアントは **、リモート****MSGSTATUS_REMOTE_DELETEプロバイダー** MSGSTATUS_REMOTE_DOWNLOADヘッダー フォルダー内のメッセージに対して、そのメッセージを設定または設定できます。 クライアント アプリケーションは、このフォルダー内の各メッセージ ヘッダーを調べて、リモート メッセージ ストアでメッセージをダウンロードするか削除するか判断できます。 次に [、IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) メソッドを使用して、適切なフラグを設定します。 **SetMessageStatus** は、このプロパティのフラグを設定する唯一の方法です。 [IMAPIProp::SetProps](imapiprop-setprops.md) メソッドは使用できません。 このプロパティを取得するには、クライアントは [IMAPIProp::GetProps ではなく IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) [を呼び出します](imapiprop-getprops.md)。
  
このプロパティのビット 16 ~ 31 (0x10000 ~ 0x80000000) は、対人間メッセージ (IPM) クライアント アプリケーションで使用できます。 その他のすべてのビットは、MAPI で使用するために予約されています。前の表で定義されていない場合は、最初は 0 に設定し、その後変更する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> サーバーとクライアント間のメッセージング オブジェクト データの同期を処理します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[IMAPITable::QueryRows](imapitable-queryrows.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

