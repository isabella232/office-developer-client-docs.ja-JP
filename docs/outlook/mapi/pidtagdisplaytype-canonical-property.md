---
title: PidTagDisplayType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e48d31ade72639adfa5ea5f9d4d2e87a201b302
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550702"
---
# <a name="pidtagdisplaytype-canonical-property"></a>PidTagDisplayType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アイコンをテーブルの特定の行に関連付けるのに使用する値を含む。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TYPE  <br/> |
|識別子:  <br/> |0x3900  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティには長整数が含まれているので、その型に基づいてテーブル エントリを特別に処理できます。 通常、この特別な処理は、表示の種類に関連付けられたアイコン、または他の表示要素を表示して構成されます。 
  
このプロパティは、フォルダーコンテンツ テーブルでは使用されません。 クライアント アプリケーションは、メッセージの **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) プロパティと適切な [IMAPIFormInfo](imapiforminfoimapiprop.md) インターフェイスを使用して、そのメッセージの **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) プロパティと **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) プロパティを取得する必要があります。 
  
このプロパティには、次のいずれかの値を指定できます。
  
DT_AGENT 
  
> 自動エージェント (Quote-Of-The-Day や天気予報グラフの表示など)。
    
DT_DISTLIST 
  
> 配布リスト。
    
DT_FOLDER 
  
> フォルダーの横に既定のフォルダー アイコンを表示します。
    
DT_FOLDER_LINK 
  
> 既定のフォルダー アイコンではなく、フォルダーの横に既定のフォルダー リンク アイコンを表示します。
    
DT_FOLDER_SPECIAL 
  
> 特殊な種類のパブリック フォルダーなど、アプリケーション固有の区別を持つフォルダーの表示アイコン。
    
DT_FORUM 
  
> 掲示板サービス、パブリック フォルダーまたは共有フォルダーなどのフォーラム。
    
DT_GLOBAL 
  
> グローバル アドレス帳。
    
DT_LOCAL 
  
> 小さなワークグループと共有するローカル アドレス帳。
    
DT_MAILUSER 
  
> 一般的なメッセージング ユーザー。
    
DT_MODIFIABLE 
  
> 変更可能。コンテナーは、ユーザー インターフェイスで変更可能として示す必要があります。
    
DT_NOT_SPECIFIC 
  
> 他の設定と一致しません。
    
DT_ORGANIZATION 
  
> ヘルプデスク、会計、血液駆動コーディネーターなど、大規模なグループに対して定義された特別なエイリアス。
    
DT_PRIVATE_DISTLIST 
  
> 個人管理の配布リスト。
    
DT_REMOTE_MAILUSER 
  
> 外部メッセージング システムまたはリモート メッセージング システムからの受信者。
    
DT_WAN 
  
> ワイド エリア ネットワーク アドレス帳。
    
アドレス帳のコンテンツ テーブルでは、DT_AGENT、DT_DISTLIST、DT_FORUM、DT_MAILUSER、DT_ORGANIZATION、DT_PRIVATE_DISTLIST、DT_REMOTE_MAILUSER の値をDT_REMOTE_MAILUSERします。 アドレス帳階層テーブルと 1 回割り当てテーブルでは、DT_GLOBAL、DT_LOCAL、DT_MODIFIABLE、DT_NOT_SPECIFIC、DT_WANが使用されます。 フォルダー階層テーブルは、DT_FOLDER、DT_FOLDER_LINK、およびDT_FOLDER_SPECIAL使用します。 
  
このプロパティを設定しない場合、クライアントはテーブルに適した既定の型 (通常はテーブル、DT_FOLDER、DT_LOCAL、またはDT_MAILUSER。 
  
 **メモ** 文書化されていないすべての値は、MAPI 用に予約されています。 クライアント アプリケーションは、新しい値を定義し、文書化されていない値を処理する準備をする必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージ オブジェクトと添付ファイル オブジェクトを処理します。
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> アドレス帳テンプレートで許容されるプロパティと操作を指定します。
    
[[MS-OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> ディレクトリ アクセスを有効にする。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

