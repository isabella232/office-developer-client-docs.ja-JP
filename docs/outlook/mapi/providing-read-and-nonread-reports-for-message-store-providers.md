---
title: メッセージストアプロバイダーに対して読み取りおよび非開封レポートを提供する
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
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>メッセージストアプロバイダーに対して読み取りおよび非開封レポートを提供する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーがメッセージを受信できる場合は、メッセージストアプロバイダーによって受信されたメッセージの読み取りレポートおよび非開封レポートをサポートする必要があります。 受信したメッセージに**PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) プロパティが含まれており、そのプロパティの値が TRUE である場合、メッセージストアは、ユーザーがメッセージを開いたときに送信者に通知メッセージを送信する必要があります。メッセージが開封されたことを示します。 同様に、ユーザーがメッセージを開く前に削除した場合は、メッセージが開封されていないことを示す返信を、メッセージストアが送信者に発行する必要があります。
  
これらのレポートを発行するには、 [IMessage: imapiprop](imessageimapiprop.md)オブジェクトを作成し、メッセージに関連するプロパティを入力して、そのメッセージがユーザーによって生成された場合と同様に MAPI スプーラーに送信します。 [imapisupport:: readreceipt](imapisupport-readreceipt.md)メソッドは、このために使用できます。 
  
> [!NOTE]
> 保留中の読み取りレポートまたは非開封レポートを含む未開封メッセージのコピーをメッセージストアが作成する場合は、特別な注意を払う必要があります。 このようなレポートは、ユーザーがレポートが要求されたメッセージのコピーを読み取るときには生成しないようにする必要があります。 このようなメッセージのコピーを作成する場合、メッセージストアプロバイダーには、 [imapifolder:: setreadflags](imapifolder-setreadflags.md)および[IMessage:: setreadflags](imessage-setreadflag.md)への呼び出しに CLEAR_RN_PENDING および CLEAR_NRN_PENDING フラグを含める必要があります。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

