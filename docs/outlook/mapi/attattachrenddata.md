---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569450"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**AttAttachRenddata**属性は、メッセージの添付ファイルを表示する場所と方法を説明する**RENDDATA**構造体としてエンコードされます。 **RENDDATA**構造体は、 **sizeof(RENDDATA)** バイトの**RENDDATA**構造体の最初のメンバーで始まるだけで TNEF ストリームにエンコードされます。 **RENDDATA**構造体の**dwFlags**のメンバーの値は、 **MAC_BINARY**に設定されている場合、次の添付ファイルのデータに格納されます MacBinary 形式です。それ以外の場合、添付ファイルのデータは、いつものようにエンコードされます。
  

