---
title: PidTagMessageCcMe 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7605739dd6d0f0205a1a4f09eb8c45d235c0c179
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329737"
---
# <a name="pidtagmessageccme-canonical-property"></a>PidTagMessageCcMe 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このメッセージングユーザーが、このメッセージの bcc 受信者として明示的に指定されていて、配布リストの一部ではない場合は、TRUE が含まれます。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|識別子:  <br/> |0x0058  <br/> |
|データの種類 :   <br/> |PT_BOOLEAN  <br/> |
|エリア:  <br/> |一般的なメッセージング  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを使用すると、リスト内のすべてのエントリを調べることなく、ユーザー名がカーボンコピー受信者一覧に明示的に表示されるかどうかを判断できます。 
  
このプロパティは、受信時の受信メッセージの自動処理にも役立ちます。 トランスポートプロバイダーのオプションでは、このプロパティに FALSE が含まれているか、またはメッセージングユーザーが受信者テーブルに直接記載されていない場合は設定されません。 
  
配布リストの展開またはブラインドカーボンコピーの指定によるメッセージ配信が、このプロパティを設定しないことがあります。 受信者は明示的に指定する必要があります。 
  
通常、未送信メッセージは、このプロパティ、 **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))、または**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) を設定しません。 ユーザーがパブリックメッセージストア、その他のユーザーのプライベートストア、ディスク上のファイル、またはその他の受信メッセージ内に埋め込まれているメッセージ内に存在する場合は、通常、トランスポートプロバイダーの最終時刻に設定された値が含まれています。メッセージを配信した。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトで許容されるプロパティと操作を指定します。
    
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

