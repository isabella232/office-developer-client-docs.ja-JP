---
title: 受信トレイへのメッセージの保存
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3df04d4e-7e80-4232-aadc-c05c99ab59cb
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 672a9df55ce711b88451a517a2813c9ad8c599ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357534"
---
# <a name="saving-a-message-in-the-inbox"></a>受信トレイへのメッセージの保存

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **受信者なしでメッセージを受信トレイに保存するには**
  
1. [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して、受信トレイのエントリ識別子を取得します。 
    
2. [IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、受信トレイを開き、そのアドレスへのポインターを取得します。 
    
3. 受信トレイの[imapifolder:: CreateMessage](imapifolder-createmessage.md)メソッドを呼び出して、メッセージを作成します。 
    
4. メッセージの[imapiprop:: setprops](imapiprop-setprops.md)メソッドを呼び出して、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))、PR_SUBJECT ()、()、 **** () を追加します ([PidTagSubject](pidtagsubject-canonical-property.md)) プロパティ。 
    
5. 各添付ファイルを作成し、そのプロパティを設定して保存します。 メッセージに添付ファイルを追加する方法の詳細については、「[メッセージの添付ファイルを作成](creating-a-message-attachment.md)する」を参照してください。
    
6. メッセージを保存するには、 **IMessage:: SaveChanges**を呼び出します。 この時点で、受信トレイのコンテンツテーブルに表示されます。 
    
受信トレイのコンテンツテーブルにメッセージを表示する前に、intermittantly メッセージを保存する場合は、代わりに、IPM サブツリーのルートフォルダーなどの隠しフォルダーで作成し、受信トレイに移動します。 
  

