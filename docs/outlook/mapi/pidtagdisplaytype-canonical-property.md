---
title: PidTagDisplayType の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3fd5a8d92621dcefce66fb42e843f78755fa84df
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802707"
---
# <a name="pidtagdisplaytype-canonical-property"></a>PidTagDisplayType の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
テーブルの特定の行にアイコンを関連付けるに使用する値が含まれています。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DISPLAY_TYPE  <br/> |
|識別子:  <br/> |0x3900  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI アドレス帳  <br/> |
   
## <a name="remarks"></a>備考

このプロパティには、その型に基づいてテーブルのエントリの特別な処理を容易にする長整数が含まれています。 この特別な処理は、通常、アイコン、または、表示の種類に関連付けられているその他の表示要素を表示するので構成されます。 
  
フォルダーの内容のテーブルでは、このプロパティは使用されません。 クライアント アプリケーションは、 **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) と**PR_MINI_ICON** ([を取得するのにメッセージのプロパティの**PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) と[IMAPIFormInfo](imapiforminfoimapiprop.md)の適切なインターフェイスを使用する必要があります。PidTagMiniIcon](pidtagminiicon-canonical-property.md)) そのメッセージのプロパティです。 
  
このプロパティは、次の値の 1 つだけ持つことができます。
  
DT_AGENT 
  
> その日の見積もりなど、自動化されたエージェントまたは気象のグラフ表示します。
    
DT_DISTLIST 
  
> 配布リスト。
    
DT_FOLDER 
  
> フォルダーの横にある既定のフォルダー アイコンを表示します。
    
DT_FOLDER_LINK 
  
> 既定のフォルダー アイコンではなく既定フォルダーのリンクのアイコンがフォルダーの横にあるを表示します。
    
DT_FOLDER_SPECIAL 
  
> パブリック フォルダーの特殊な型など特定のアプリケーションの違いは、のフォルダーのアイコンを表示します。
    
DT_FORUM 
  
> フォーラム、掲示板サービスなど、パブリック フォルダーまたは共有フォルダーです。
    
DT_GLOBAL 
  
> グローバル アドレス帳です。
    
DT_LOCAL 
  
> 少人数のワークグループと共有しているローカルのアドレス帳です。
    
DT_MAILUSER 
  
> 一般的なメッセージングのユーザーです。
    
DT_MODIFIABLE 
  
> 変更可能です。コンテナーは必要がありますと変更可能なユーザー ・ インタ フェースで示されます。
    
DT_NOT_SPECIFIC 
  
> 他の設定のいずれかが一致しません。
    
DT_ORGANIZATION 
  
> ヘルプデスク、会計、または血のドライブのコーディネーターなど、大規模なグループに対して定義されている特殊なエイリアスです。
    
DT_PRIVATE_DISTLIST 
  
> プライベートは、個人的には配布リストを管理します。
    
DT_REMOTE_MAILUSER 
  
> 既知の外部またはリモートのメッセージング システムから受信者です。
    
DT_WAN 
  
> ワイド エリア ネットワークのアドレス帳です。
    
アドレス帳の内容のテーブルでは、DT_AGENT、DT_DISTLIST、DT_FORUM、DT_MAILUSER、DT_ORGANIZATION、DT_PRIVATE_DISTLIST、および DT_REMOTE_MAILUSER の値を使用します。 アドレス帳階層テーブルと一時テーブルは、DT_GLOBAL、DT_LOCAL、DT_MODIFIABLE、DT_NOT_SPECIFIC、および DT_WAN の値を使用します。 フォルダーの階層テーブルには、DT_FOLDER、DT_FOLDER_LINK、DT_FOLDER_SPECIAL の値を使用します。 
  
このプロパティが設定されていない場合、クライアントを想定してください既定の型、テーブル、通常 DT_FOLDER、DT_LOCAL、または DT_MAILUSER の適切です。 
  
 **メモ**記載されていないすべての値は、MAPI 用に予約されています。 クライアント アプリケーションは、新しい値を定義する必要がないと、文書化されていない値で対処するために準備する必要があります。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> メッセージと添付ファイルのオブジェクトを処理します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティは、アドレス帳のテンプレートの許可の操作を指定します。
    
[[MS OXLDAP]](http://msdn.microsoft.com/library/727c090a-f05c-4eed-94aa-565724cfc550%28Office.15%29.aspx)
  
> ディレクトリのアクセスを有効にします。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

