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
ms.openlocfilehash: d8c6699ac1bc5687b1c885d156535e5b54b93140
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799707"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**適用されます**: Outlook 
  
**AttAttachRenddata**属性は、メッセージの添付ファイルを表示する場所と方法を説明する**RENDDATA**構造体としてエンコードされます。 **RENDDATA**構造体は、 **sizeof(RENDDATA)** バイトの**RENDDATA**構造体の最初のメンバーで始まるだけで TNEF ストリームにエンコードされます。 **RENDDATA**構造体の**dwFlags**のメンバーの値は、 **MAC_BINARY**に設定されている場合、次の添付ファイルのデータに格納されます MacBinary 形式です。それ以外の場合、添付ファイルのデータは、いつものようにエンコードされます。
  

