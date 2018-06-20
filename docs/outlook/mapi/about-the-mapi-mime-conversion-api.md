---
title: MAPI から MIME 変換 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 43ce3ecea6b80bace2bcc2bd333b5c1839514f7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799608"
---
# <a name="about-the-mapi-mime-conversion-api"></a>MAPI から MIME 変換 API について

  
  
**適用されます**: Outlook 
  
MAPI から MIME 変換 API では、MAPI メッセージの MIME のオブジェクトとの間で変換するメール プロバイダーを使用します。 定数の定義、クラス識別子、および[MAPI の定数](mapi-constants.md)のように、インターフェイス識別子を提供します。 メール プロバイダーでは、 **CoCreateInstance**関数を呼び出すことによって、 **[IConverterSession](iconvertersessioniunknown.md)** のインスタンスを作成する必要があります。 
  

