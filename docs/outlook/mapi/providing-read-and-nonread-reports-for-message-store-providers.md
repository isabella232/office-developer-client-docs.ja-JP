---
title: メッセージ ストア プロバイダー用の開封済みレポートと未開封レポートの提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803738"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>メッセージ ストア プロバイダー用の開封済みレポートと未開封レポートの提供

  
  
**適用対象**: Outlook 
  
メッセージ ストア プロバイダーはメッセージを受信する場合に、読み取りとメッセージ ストア プロバイダーによって受信されたメッセージの nonread のレポートをサポートする必要があります。 メッセージ ・ ストアは、ユーザーが、メッセージを開いたとき、ソース ファイルを送信者に通知メッセージを送信**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) のプロパティが受信したメッセージに含まれている場合は、そのプロパティの値は TRUE をメッセージが読み取られたことを示します。 同様に、ユーザーは、開く前に、メッセージを削除した場合、メッセージ ・ ストアする必要がありますメッセージが読まれていることを示す送信者への応答を発行します。
  
作成するだけではこれらのレポートを発行、 [IMessage: IMAPIProp](imessageimapiprop.md)オブジェクト、メッセージ、関連するプロパティを入力し、メッセージは、ユーザーによって作成されたものがあるかのように、MAPI スプーラーに送信します。 この[IMAPISupport::ReadReceipt](imapisupport-readreceipt.md)メソッドを使用できます。 
  
> [!NOTE]
> 特別な注意する必要があるメッセージ ストアは、未読のメッセージを保留中の読み取りまたは nonread のレポートのコピーを作成するとき。 ユーザーはレポートが要求されたメッセージのコピーを読み取るときに、このようなレポートを生成できませんする必要があります。 とき、このようなメッセージのコピーを作成するには、メッセージ ストア プロバイダーは、 [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)と[IMessage::SetReadFlag](imessage-setreadflag.md)への呼び出しで、CLEAR_RN_PENDING と CLEAR_NRN_PENDING フラグを含める必要があります。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

