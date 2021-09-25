---
title: ����̃��[���̕ۑ��ꏊ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6f25fdeb176b2d885a4ba3fbf2bfb8b094de223f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576416"
---
# <a name="default-message-stores"></a>既定のメッセージ ストア

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
A default message store is one that client applications can use for general purpose messaging tasks. There are a number of optional features for message store providers that become required if the message store provider is to be used as the default message store. They are as follows:
  
- Implementing the special folders: the Inbox, Outbox, and search-results folders.
    
- �J���� nonread �̃��|�[�g��񋟂��܂��B
    
- ���M����є��M�������b�Z�[�W�̑��M������܂��B
    
- �N���X�̔C�ӂ̃��b�Z�[�W����b�Z�[�W�̍쐬������܂��B
    
- ���O�t���ƕ����l�̃v���p�e�B��T�|�[�g���܂��B
    
- Supporting the [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) method, even if the message store provider is tightly coupled with a transport provider. 
    
- �֘A����R���e���c�̃e�[�u����T�|�[�g���܂��B�ڍׂɂ��ẮA [�e�[�u���ȓ�e](contents-tables.md)��Q�Ƃ��Ă��������B
    
- 送信メッセージ キューにメッセージがある場合に、MAPI スプーラーの通知をサポートします。
    
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

