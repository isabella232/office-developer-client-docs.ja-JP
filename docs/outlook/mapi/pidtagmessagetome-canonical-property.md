---
title: PidTagMessageToMe の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageToMe
api_type:
- HeaderDef
ms.assetid: aeb0fa71-f471-46c5-ad9c-f8afb3fed533
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 42aec7a8d617bdf1abd385add30d903efa2b73d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802998"
---
# <a name="pidtagmessagetome-canonical-property"></a>PidTagMessageToMe の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
このメッセージング ユーザーが具体的には (このメッセージの受信者宛先) プライマリという配布リストの一部ではない場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_MESSAGE_TO_ME  <br/> |
|識別子:  <br/> |0x0057  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |メッセージ全般  <br/> |
   
## <a name="remarks"></a>備考

このプロパティを確認するかどうかユーザー名に明示的に、プライマリ受信者ボックスの一覧で、リスト内のすべてのエントリを検査せずに便利な方法を提供します。 
  
このプロパティは、受信したメッセージの受信確認の時点での自動処理を支援します。 トランスポート プロバイダーのオプションでは、このプロパティは FALSE が含まれて か、またはメッセージングのユーザーが受信者テーブルに直接表示されていない場合は含まれていません。 
  
配布リストの展開またはブラインド カーボン コピーの指定によるメッセージの配信は、このプロパティを設定するには発生しません。 受信者は明示的に指定する必要があります。 
  
未送信メッセージ一般には設定されません ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))、 **PR_MESSAGE_CC_ME** 、 **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))、またはこのプロパティ。 ユーザーがアクセスできる他のユーザーのプライベート、パブリック メッセージ ストアに、ディスク上のファイル ストアまたはその他の受信したメッセージ内に埋め込まれている、一般に含まれている値を設定したメッセージ内に存在する場合は、前回のトランスポート プロバイダーメッセージを配信します。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> プロパティは、電子メール メッセージのオブジェクトに対して許可する操作を指定します。
    
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
