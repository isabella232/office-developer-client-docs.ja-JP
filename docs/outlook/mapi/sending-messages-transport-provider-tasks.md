---
title: ���b�Z�[�W�̑��M �g�����X�|�[�g �v���o�C�_�[�̃^�X�N
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: fa25f575e55eb3d0446148d75de314a8883a4170
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591179"
---
# <a name="sending-messages-transport-provider-tasks"></a>メッセージの送信: トランスポート プロバイダーのタスク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **�g�����X�|�[�g �v���o�C�_�[�A���b�Z�[�W�𑗐M����ɂ�**
  
- トランスポート プロバイダーがメッセージ **を送信した後、** またはメッセージの送信を試行した後、メッセージの PR_RESPONSIBILITY ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) プロパティを TRUE に設定します。 If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. メッセージが正常に送信され **、PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested)](pidtagoriginatordeliveryreportrequested-canonical-property.md)プロパティが TRUE に設定されている場合は、成功した受信者を含む [ADRLIST](adrlist.md) 構造体を作成し、それぞれに **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) プロパティを設定し **、StatusRecips** を呼び出して配信レポートを生成します。 For more information about creating delivery and non-delivery reports, see the following topics: [MAPI Report Messages](mapi-report-messages.md), [Required Report Message Properties](required-report-message-properties.md), [Optional Report Message Properties](optional-report-message-properties.md), and [Sending Message Delivery Reports](sending-message-delivery-reports.md).
    
- メッセージの **プロパティグループPR_SENDER** ログオンしているユーザーの ID に設定します。 このグループには **、PR_SENDER_ENTRYID** ([PidTagSenderEntryId)](pidtagsenderentryid-canonical-property.md) **、PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md) **)、PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **)、PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))、PR_SENDER_EMAIL_ADDRESS ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) が含まれます。 
    
- �\�ł���΁A���O�I�����Ă��郆�[�U�[�� id�A�܂��͑㗝�l���L���ȃ��[�U�[�ɂ́A���b�Z�[�W�� **PR_SENT_REPRESENTING**�̃v���p�e�B��ݒ肵�܂��B **PR_SENT_REPRESENTING**�v���p�e�B�́A���̃��[�U�[�̑㗝�Ƃ��āA���b�Z�[�W�̑��M���������A1 �̃��[�U�[���g�p����܂��B�����̃v���p�e�B��T�|�[�g���Ă��Ȃ��g�����X�|�[�g �v���o�C�_�[�𖳎����đ��M���b�Z�[�W�ɂ��܂��B 
    
- クライアントが [IMessage::SubmitMessage](imessage-submitmessage.md)を呼び出す **PR_CLIENT_SUBMIT_TIMEメッセージの** プロパティ [(PidTagClientSubmitTime)](pidtagclientsubmittime-canonical-property.md)プロパティを設定します。
    
- メッセージ ストア プロバイダーがメッセージを **送信** 済みとしてマークした日時を示すために、メッセージの PR_PROVIDER_SUBMIT_TIME ([PidTagProviderSubmitTime)](pidtagprovidersubmittime-canonical-property.md)プロパティを設定します。 
    
���܂��܂ȃ��b�Z�[�W���O �V�X�e����������̎�M�҂Ƀ��b�Z�[�W�����M�����ƁA���M���ꂽ�e�R�s�[�ɂ́A���܂��܂ȑ��M�� id ������܂��B 
  
The transport provider or tightly coupled message store and transport is also responsible for setting originator and reply-to information. Originator information is stored in the **PR_ORIGINATOR** properties and reply-to information is stored in the PR_REPLY properties. The client can set these properties; however, the transport provider is allowed to ignore and overwrite the client's settings. 
  

