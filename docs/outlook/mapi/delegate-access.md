---
title: �㗝�l�A�N�Z�X
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a863494f-0071-4d97-a6c4-26707ee00e04
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d969fd806e5038e6c918da45041402a981554a49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799903"
---
# <a name="delegate-access"></a>�㗝�l�A�N�Z�X

  
  
**適用対象**: Outlook 
  
代理人アクセスは、別のユーザーとしてメッセージを送信または別のユーザーに対してメッセージが表示するユーザーのことを指します。 代理人アクセスは、mapi トランスポート プロバイダーは、選択した場合をサポートできるサービス プロバイダーに依存しない機能です。 ただし、これを行うプロバイダーは必要ありません。 代理人アクセスは、ユーザーとして、メッセージを送信したり、別のユーザーまたはユーザーが別のユーザーのメッセージ ストアにアクセスする必要があるときの受信メッセージをフィルター処理する必要がある場合に重要です。 他のユーザーのストアに接続するための代理ユーザーを許可する前に、メッセージ ストア プロバイダーは代理人ユーザーが適切な権限を持っているを確認する必要があります。 
  
�㗝�l�A�N�Z�X��T�|�[�g���邽�߂Ɏg�p����v���p�e�B�� 2 �̃O���[�v������܂��B
  
 **PR_SENT_REPRESENTING_ADDRTYPE**([PidTagSentRepresentingAddressType](pidtagsentrepresentingaddresstype-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_EMAIL_ADDRESS**([PidTagSentRepresentingEmailAddress](pidtagsentrepresentingemailaddress-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_ENTRYID**([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_NAME**([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md)) 
  
 **PR_SENT_REPRESENTING_SEARCH_KEY**([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ADDRTYPE**([PidTagReceivedRepresentingAddressType](pidtagreceivedrepresentingaddresstype-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_EMAIL_ADDRESS**([PidTagReceivedRepresentingEmailAddress](pidtagreceivedrepresentingemailaddress-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_ENTRYID**([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_NAME**([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md)) 
  
 **PR_RCVD_REPRESENTING_SEARCH_KEY**([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md)) 
  
送信メッセージは、 **PR_SENT_REPRESENTING**プロパティは、送信者として機能する必要があるメッセージングのユーザーを識別します。 クライアントは、オプションとしてこれらのプロパティを設定することができます。 時間によっては、 **PR_SENT_REPRESENTING**プロパティは設定されていない場合は、メッセージは代理人のアクセスをサポートするトランスポート プロバイダーに到達、 **PR_SENDER**のプロパティ設定を行うため、プロバイダーの責任です。 
  
��M���b�Z�[�W�ɂ́A **PR_RCVD_REPRESENTING**�v���p�e�B�́A��M�҂Ƃ��ċ@�\����K�v������܂����[�U�[����肵�܂��B�㗝�l�̃��b�Z�[�W��z�M����ӔC�g�����X�|�[�g �v���o�C�_�[�́A **PR_RCVD_REPRESENTING**�� **PR_RECEIVED_BY**�̗����̃v���p�e�B��ݒ肷��K�v������܂��B�N���C�A���g�́A�㗝�l�̃��b�Z�[�W���M�́A�Ή����� **PR_RCVD_REPRESENTING**�v���p�e�B�� **PR_SENT_REPRESENTING**�v���p�e�B�̒l��R�s�[����K�v������܂��B 
  
���Ƃ��΁A�T���[���x�ɒ��ɁAJohn �� Sally �̃��b�Z�[�W����M����Ƃ��܂��B **PR_RCVD_REPRESENTING**�v���p�e�B�́A�㗝�l�̈���Ƃ��� John ����肵�܂��BJohn Sally �̔ގ�M�������b�Z�[�W�ւ̕ԐM�𑗐M���郁�b�Z�[�W�� **PR_SENDER**�v���p�e�B�́A���o�l�Ƃ��� John ����肵�܂��BJohn Sally ��\�����A���邽�߂ɁA **PR_SENT_REPRESENTING**�v���p�e�B�� Sally ����肵�܂��B 
  
代理人の受信メッセージを処理する必要があります**PR_SENDER**プロパティによって識別されるユーザーとしてではなく、 **PR_SENT_REPRESENTING**プロパティで識別されるメッセージングのユーザーとしてこれらのメッセージ配信通常プロバイダーに転送します。 この規則の例外は、アクセス権限およびトランスポートの種類に一致する必要がある場合です。 この例では、トランスポート プロバイダーは、送信側の id を選択できます。 
  
**PR_SENT_REPRESENTING**プロパティが、代理人の受信メッセージに使用できる場合は、配信を処理するトランスポート プロバイダーは、これらの値は、 **PR_SENDER**の対応するプロパティの値を使用します。 **PR_SENT_REPRESENTING**プロパティが使用できるトランスポート プロバイダーが [代理人アクセスをサポートしていない場合は、配信の**PR_SENDER**プロパティを使用できます。 
  

