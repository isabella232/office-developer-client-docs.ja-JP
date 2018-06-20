---
title: 文字の文字列を使用してフォルダーの名前付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a6ea37bf573dab996b5a8fd7886a76fddd5b98ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801662"
---
# <a name="naming-folders-by-using-character-strings"></a>文字の文字列を使用してフォルダーの名前付け

  
  
**適用されます**: Outlook 
  
セッション中に頻繁に 1 つまたは複数のフォルダーにアクセスする場合は、 [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)メソッドを使用してフォルダーに名前を割り当てることを検討してください。 **IMsgStore::SetReceiveFolder**を使用して、特定のメッセージ クラスのメッセージを受信する特別なフォルダーを設定するには、主に、名前を持つ任意のフォルダーを関連付けるには、使用できます。 メッセージ クラスと同じ名前は、または任意の文字列をクライアントの使用に合わせてカスタマイズできます。 フォルダーに名前を関連付けることを検索して、フォルダーを開くにかかる時間が減少します。 
  

