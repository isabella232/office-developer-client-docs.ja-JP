---
title: 'title: "��\���ɂ��� MAPI �t�H���_�[" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1
description: 'COM ms.assetid: 8b3b9c80-f7f4-4f37-bd6b-323469d020f1 description: "�ŏI�X�V��: 2011�N7��23��"'
ms.openlocfilehash: cb09c8b3406632f97b128a1bed8a5f0a88298d2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561237"
---
# <a name="mapi-hidden-folders"></a>title: "��\���ɂ��� MAPI �t�H���_�[" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
Hidden folders are generic folders that clients create in the root folder of the message store, rather than in the root folder of an interpersonal message (IPM) subtree. Because these folders are not placed in an IPM subtree, they are generally hidden from the user's view by the message store provider. Hidden folders typically contain information that is relevant to the message store but irrelevant to the user. Clients create hidden folders to store, for example, additional information to be saved with the rest of the folder hierarchy.
  
MAPI expects all clients to be able to display, create, modify, and delete folders in an IPM subtree. Support for working with folders in other trees is considered optional. However, all message stores that can be used as the default store and that can send and receive messages should fully support hidden folders.
  
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

