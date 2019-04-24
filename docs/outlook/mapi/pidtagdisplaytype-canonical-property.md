---
title: PidTagDisplayType 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayType
api_type:
- HeaderDef
ms.assetid: ee2bc6ca-3769-4b56-a77d-81418d28f768
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: da26fd2a8643817cf60adbfa6f4e85da345b875c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360782"
---
# <a name="pidtagdisplaytype-canonical-property"></a>PidTagDisplayType 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表の特定の行にアイコンを関連付けるために使用される値を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DISPLAY_TYPE  <br/> |
|識別子:  <br/> |0x3900  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>解説

このプロパティには、その種類に基づいてテーブルエントリの特別な処理を容易にする長整数型 (long) の値が含まれています。 この特別な処理では、通常、表示の種類に関連付けられたアイコンまたはその他の表示要素が表示されます。 
  
このプロパティは、フォルダーの内容の表では使用されません。 クライアントアプリケーションは、メッセージの**PR_MESSAGE_CLASS** (PidTagMessageClass) プロパティと適切な[imapiforminfo](imapiforminfoimapiprop.md)インターフェイスを使用して、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) と**PR_MINI_ICON** ([](pidtagmessageclass-canonical-property.md)) を取得する必要があります ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) そのメッセージのプロパティ。 
  
このプロパティには、次のいずれかの値を指定できます。
  
DT_AGENT 
  
> 自動エージェント (見積書など) または天気予報チャートが表示されます。
    
DT_DISTLIST 
  
> 配布リスト。
    
DT_FOLDER 
  
> フォルダーの横に既定のフォルダーアイコンを表示します。
    
DT_FOLDER_LINK 
  
> 既定のフォルダーアイコンではなく、フォルダーの横に既定のフォルダーリンクアイコンを表示します。
    
DT_FOLDER_SPECIAL 
  
> 特別な種類のパブリックフォルダーなど、アプリケーション固有の区別があるフォルダーのアイコンを表示します。
    
DT_FORUM 
  
> 掲示板サービス、公共または共有フォルダーなどのフォーラム。
    
DT_GLOBAL 
  
> グローバルアドレス帳。
    
DT_LOCAL 
  
> 小さなワークグループと共有しているローカルアドレス帳。
    
DT_MAILUSER 
  
> 一般的なメッセージングユーザー。
    
DT_MODIFIABLE 
  
> 可能コンテナーは、ユーザーインターフェイスで変更可能として表示される必要があります。
    
DT_NOT_SPECIFIC 
  
> 他の設定と一致しません。
    
DT_ORGANIZATION 
  
> ヘルプデスク、経理、または血圧のコーディネーターなど、大規模なグループに定義された特別なエイリアス。
    
DT_PRIVATE_DISTLIST 
  
> 個人が管理する私的な配布リスト。
    
DT_REMOTE_MAILUSER 
  
> 外部またはリモートのメッセージングシステムからの受信者であることがわかっている受信者。
    
DT_WAN 
  
> ワイドエリアネットワークのアドレス帳。
    
アドレス帳の内容の表では、DT_AGENT、DT_DISTLIST、DT_FORUM、DT_MAILUSER、DT_ORGANIZATION、DT_PRIVATE_DISTLIST、および DT_REMOTE_MAILUSER の値を使用します。 アドレス帳階層テーブルと1回限りのテーブルは、DT_GLOBAL、DT_LOCAL、DT_MODIFIABLE、DT_NOT_SPECIFIC、DT_WAN の各値を使用します。 フォルダー階層テーブルは、DT_FOLDER、DT_FOLDER_LINK、および DT_FOLDER_SPECIAL の値を使用します。 
  
このプロパティが設定されていない場合、クライアントは、テーブルに適した既定の種類 (通常は、DT_FOLDER、DT_LOCAL、または DT_MAILUSER) を想定する必要があります。 
  
 **メモ**文書化されていないすべての値は MAPI 用に予約されています。 クライアントアプリケーションは、新しい値を定義せず、文書化されていない値を処理するために準備する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルオブジェクトを処理します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> アドレス帳テンプレートで許容されるプロパティと操作を指定します。
    
[[OXLDAP]](https://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> ディレクトリアクセスを有効にします。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

