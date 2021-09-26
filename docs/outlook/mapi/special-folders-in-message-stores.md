---
title: ���[���̕ۑ��ꏊ�œ��ʂȃt�H���_�[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9462070e-1472-4e12-ba4e-e4ac60022892
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 453aaa842b9b69d5eaf502f85cd5b3c2b655b673
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591074"
---
# <a name="special-folders-in-message-stores"></a>���[���̕ۑ��ꏊ�œ��ʂȃt�H���_�[

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Special folders such as the Inbox, Outbox, and search-results folder may be created in advance and protected by the message store provider. If the folders do not exist, MAPI will attempt to create them in the message store by calling the [HrValidateIPMSubtree](hrvalidateipmsubtree.md) function. For more information, see [MAPI Special Folders](mapi-special-folders.md).
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのフォルダーの実装](implementing-folders-in-message-stores.md)

