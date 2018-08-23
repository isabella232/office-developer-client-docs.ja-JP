---
title: 文字列を使用してフォルダーに名前を付ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594587"
---
# <a name="naming-folders-by-using-character-strings"></a>文字列を使用してフォルダーに名前を付ける

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
セッション中に頻繁に 1 つまたは複数のフォルダーにアクセスする場合は、 [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)メソッドを使用してフォルダーに名前を割り当てることを検討してください。 **IMsgStore::SetReceiveFolder**を使用して、特定のメッセージ クラスのメッセージを受信する特別なフォルダーを設定するには、主に、名前を持つ任意のフォルダーを関連付けるには、使用できます。 メッセージ クラスと同じ名前は、または任意の文字列をクライアントの使用に合わせてカスタマイズできます。 フォルダーに名前を関連付けることを検索して、フォルダーを開くにかかる時間が減少します。 
  

