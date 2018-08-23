---
title: ���b�Z�[�W�̑��M �g�����X�|�[�g �v���o�C�_�[�̃^�X�N
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 2c1f73ab263e5851c78b33b6157d6d44c9e5e404
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586229"
---
# <a name="sending-messages-transport-provider-tasks"></a>���b�Z�[�W�̑��M: �g�����X�|�[�g �v���o�C�_�[�̃^�X�N

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **�g�����X�|�[�g �v���o�C�_�[�A���b�Z�[�W�𑗐M����ɂ�**
  
- トランスポート プロバイダーがメッセージを送信またはメッセージを送信しようとしてください。 後は、true を指定するメッセージの**れない**([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) のプロパティを設定します。 メッセージを送信しようとすると、失敗した場合、トランスポート プロバイダーは、配信不能レポートを生成する[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)を呼び出す必要があります。 **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) プロパティが TRUE に設定されてメッセージが正常に送信された場合、失敗した受信者を含む[ADRLIST](adrlist.md)構造を作成します。ごとに、 **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) のプロパティを設定し、配信レポートを生成するのには**StatusRecips**を呼び出します。 配信し、配信不能レポートを作成する方法の詳細については、次のトピックを参照してください: [MAPI レポート メッセージ](mapi-report-messages.md)、[レポート メッセージのプロパティのために必要な](required-report-message-properties.md)[オプションのレポート メッセージのプロパティ](optional-report-message-properties.md)、および[送信メッセージの配信レポート](sending-message-delivery-reports.md)。
    
- ログオンしているユーザーの id をメッセージの**PR_SENDER**のグループのプロパティを設定します。 このグループが含まれています: **PR_SENDER_ADDRTYPE** ([ 、 **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))、 **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))、 **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md))、および**PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md))。
    
- �\�ł���΁A���O�I�����Ă��郆�[�U�[�� id�A�܂��͑㗝�l���L���ȃ��[�U�[�ɂ́A���b�Z�[�W�� **PR_SENT_REPRESENTING**�̃v���p�e�B��ݒ肵�܂��B **PR_SENT_REPRESENTING**�v���p�e�B�́A���̃��[�U�[�̑㗝�Ƃ��āA���b�Z�[�W�̑��M���������A1 �̃��[�U�[���g�p����܂��B�����̃v���p�e�B��T�|�[�g���Ă��Ȃ��g�����X�|�[�g �v���o�C�_�[�𖳎����đ��M���b�Z�[�W�ɂ��܂��B 
    
- メッセージの**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) を示すプロパティをクライアントに[IMessage::SubmitMessage](imessage-submitmessage.md)が呼び出されたときに設定します。
    
- メッセージ ストア プロバイダーは、メッセージとして送信されたことをマークするときの日時を示すメッセージの**PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) のプロパティを設定します。 
    
���܂��܂ȃ��b�Z�[�W���O �V�X�e����������̎�M�҂Ƀ��b�Z�[�W�����M�����ƁA���M���ꂽ�e�R�s�[�ɂ́A���܂��܂ȑ��M�� id ������܂��B 
  
トランスポート プロバイダーまたは密結合のメッセージ ・ ストアおよびトランスポートでは、差出人および返信先情報の設定を行いますもします。 発信者情報は、 **PR_ORIGINATOR**プロパティと PR_REPLY プロパティで返信する情報が格納されています。 クライアントは、これらのプロパティを設定できます。ただし、トランスポート プロバイダーは許可を無視し、クライアントの設定を上書きします。 
  

