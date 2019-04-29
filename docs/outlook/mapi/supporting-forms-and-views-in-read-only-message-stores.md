---
title: �ǂݎ���p�̃��b�Z�[�W �X�g�A�ł̃t�H�[���ƃr���[�̃T�|�[�g
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: da5f080d-4397-4ce6-8561-73dd13445e77
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0b7ffe07278cfcbba95351f2720e427dd8500221
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432430"
---
# <a name="supporting-forms-and-views-in-read-only-message-stores"></a>�ǂݎ���p�̃��b�Z�[�W �X�g�A�ł̃t�H�[���ƃr���[�̃T�|�[�g

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
If your message store provider allows read-only permission to the underlying storage mechanism, client applications and the MAPI form manager will be unable to do certain things. Specifically, clients will be unable to add or modify custom views, and the MAPI form manager will be unable to install forms in the associated contents tables of the store's folders.
  
For many read-only message stores, that may not be a problem. If that is the case, the message store provider does not need to support associated contents tables at all. However, if your message store provider must be read-only and it must also support a predefined set of views or forms, it will need to support associated contents tables.
  
The most common strategy for doing this, because clients and the MAPI form manager cannot install the views or forms into the message store themselves, is for the message store provider to hard-code them into the message store. This means that the associated contents table or tables that contain the views or forms will exist in the message store when it is created, before any clients or the MAPI form manager ever access it. Then, when a client requests an associated contents table to get custom views from a form or the MAPI form manager requests an associated contents table to launch a form, the message store provider can provide one. 
  
This requirement that the associated contents tables be created and populated when the message store itself is created implies that your message store provider will need to obtain information about the format of the special messages that clients and the MAPI form manager use to store views and forms. What those formats are will depend on the client and MAPI form manager being used, so a description of them cannot be provided here.
  
## <a name="see-also"></a>関連項目



[�ǂݎ���p�̃��b�Z�[�W�̕ۑ�](read-only-message-stores.md)

