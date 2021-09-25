---
title: ���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a2b418cb0a075a27b3f319a7790007b4774c0aa7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624098"
---
# <a name="supporting-named-properties-in-message-stores"></a>���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Message objects can have properties in them that are not in the set of properties defined by MAPI. Such properties can be unnamed or named. Unnamed properties must reside in a range of property identifiers defined by MAPI. Named custom properties reside in a different range of property identifiers defined by MAPI. They are typically used by custom message types. Your message store provider must support named properties if it is to be used as the default message store. Supporting named properties means implementing the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods, and implementing one or more mapping signatures that identify what names go with what property identifiers. For more information, see [Defining New MAPI Properties](defining-new-mapi-properties.md) and [Supporting Named Properties](supporting-named-properties.md).
  
Most message store providers that support named properties use a single mapping signature for all objects in the message store. This has two benefits. First, it is simpler to implement mapping signatures if there is only one to keep track of. Second, if all objects in the message store use the same mapping signature, client applications are assured that all property identifiers on messages in the message store actually refer to the same named property. This enables client applications to display columns for named properties in their folder view interface.
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのメッセージの実装](implementing-messages-in-message-stores.md)

