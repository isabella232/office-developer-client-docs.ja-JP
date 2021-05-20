---
title: メッセージ ストア プロバイダーに対する読み取りレポートと読み取り以外のレポートの提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432339"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>メッセージ ストア プロバイダーに対する読み取りレポートと読み取り以外のレポートの提供

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーがメッセージを受信できる場合は、メッセージ ストア プロバイダーが受信したメッセージの読み取りレポートと未読レポートをサポートする必要があります。 受信メッセージに **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested)](pidtagreadreceiptrequested-canonical-property.md)プロパティが含まれている場合、そのプロパティの値が TRUE の場合、メッセージ ストアは、ユーザーがメッセージを開くと送信者に通知メッセージを送信し、メッセージが読み取られたことを示す必要があります。 同様に、ユーザーがメッセージを開く前に削除した場合、メッセージ ストアは、メッセージが読み取りなかったことを示す返信を送信者に発行する必要があります。
  
これらのレポートの発行は [、IMessage : IMAPIProp](imessageimapiprop.md) オブジェクトを作成し、メッセージに関連するプロパティを入力し、メッセージがユーザーに送信された場合と同様に MAPI スプーラーに送信する問題です。 この [場合、IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) メソッドを使用できます。 
  
> [!NOTE]
> メッセージ ストアが未読メッセージのコピーを、保留中の読み取りレポートまたは未読レポートと一緒に作成する場合は、特別な注意が必要です。 このようなレポートは、ユーザーが要求されたメッセージのコピーを読み取った場合に生成される必要があります。 このようなメッセージのコピーを作成する場合、メッセージ ストア プロバイダーは [、IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) および [IMessage::SetReadFlag](imessage-setreadflag.md)への呼び出しに CLEAR_RN_PENDING フラグと CLEAR_NRN_PENDING フラグを含める必要があります。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

