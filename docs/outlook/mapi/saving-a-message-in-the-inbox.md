---
title: 受信トレイにメッセージを保存する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6f163f2bbcb106e5341d34e616c79efb970c1a55
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578761"
---
# <a name="saving-a-message-in-the-inbox"></a>受信トレイにメッセージを保存する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **受信者を含めずにメッセージを受信トレイに保存するには**
  
1. 受信 [トレイのエントリ識別子を取得するには、IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) を呼び出します。 
    
2. [IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出して受信トレイを開き、その受信トレイへのポインターを取得します。 
    
3. 受信トレイの [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) メソッドを呼び出して、メッセージを作成します。 
    
4. メッセージの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを呼び出 **して、PR_BODY** [(PidTagBody)、PR_HTML](pidtagbody-canonical-property.md)[(PidTagHtml)、](pidtaghtml-canonical-property.md)または **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティと **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティを追加します。  
    
5. 各添付ファイルを作成し、そのプロパティを設定し、保存します。 メッセージへの添付ファイルの追加の詳細については、「メッセージ添付ファイルの作成 [」を参照してください](creating-a-message-attachment.md)。
    
6. **IMessage::SaveChanges を呼び出して** メッセージを保存します。 この時点で、受信トレイのコンテンツ テーブルに表示されます。 
    
メッセージを受信トレイのコンテンツ テーブルに表示する前に、メッセージを間で保存する場合は、IPM サブツリーのルート フォルダーなどの非表示フォルダーにメッセージを作成し、受信トレイに移動します。 
  

