---
title: MAPI-MIME 会話 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7123b2deaa9ae0f26002b486df229ad589009f53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321820"
---
# <a name="about-the-mapi-mime-conversion-api"></a>MAPI-MIME 会話 API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi-mime 変換 API を使用すると、メールプロバイダーは MIME オブジェクトと MAPI メッセージ間で変換することができます。 このメソッドは、 [MAPI 定数](mapi-constants.md)に示されているように、定数定義、クラス識別子、およびインターフェイス識別子を提供します。 メールプロバイダーは、 **CoCreateInstance**関数を呼び出すことによって、 **[iconvertersession](iconvertersessioniunknown.md)** のインスタンスを cocreate する必要があります。 
  

