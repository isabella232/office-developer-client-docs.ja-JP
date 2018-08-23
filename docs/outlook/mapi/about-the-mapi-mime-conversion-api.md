---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575267"
---
# <a name="about-the-mapi-mime-conversion-api"></a>MAPI-MIME 会話 API について

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI から MIME 変換 API では、MAPI メッセージの MIME のオブジェクトとの間で変換するメール プロバイダーを使用します。 定数の定義、クラス識別子、および[MAPI の定数](mapi-constants.md)のように、インターフェイス識別子を提供します。 メール プロバイダーでは、 **CoCreateInstance**関数を呼び出すことによって、 **[IConverterSession](iconvertersessioniunknown.md)** のインスタンスを作成する必要があります。 
  

