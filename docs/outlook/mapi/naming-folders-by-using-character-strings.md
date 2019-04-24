---
title: 文字列を使用してフォルダーに名前を付ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 49ffe6b45002aec6660130132321559fc07c01c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326251"
---
# <a name="naming-folders-by-using-character-strings"></a>文字列を使用してフォルダーに名前を付ける

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション中に頻繁に1つ以上のフォルダーにアクセスする場合は、 [IMsgStore:: setreceivefolder](imsgstore-setreceivefolder.md)メソッドを使用してフォルダーに名前を割り当てることを検討してください。 **IMsgStore:: setreceivefolder**は、主に特定のメッセージクラスに対する受信メッセージを受信する特別なフォルダーを確立するために使用されますが、任意のフォルダーを名前に関連付けるためにも使用できます。 この名前は、メッセージクラスと同じにすることも、クライアントの使用に合わせてカスタマイズされた任意の文字文字列にすることもできます。 フォルダーに名前を関連付けると、フォルダーを見つけて開くのにかかる時間が短縮されます。 
  

