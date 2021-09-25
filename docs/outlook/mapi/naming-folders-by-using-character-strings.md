---
title: 文字列を使用してフォルダーに名前を付ける
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 23fb125218923f823593c8d40694eb1337366289
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556022"
---
# <a name="naming-folders-by-using-character-strings"></a>文字列を使用してフォルダーに名前を付ける

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション中に頻繁に 1 つ以上のフォルダーにアクセスする場合は [、IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) メソッドを使用してフォルダーに名前を割り当てすることを検討してください。 **IMsgStore::SetReceiveFolder** は、主に特定のメッセージ クラスの受信メッセージを受信するための特別なフォルダーを確立するために使用しますが、任意のフォルダーを名前に関連付ける場合にも使用できます。 名前はメッセージ クラスと同じにするか、クライアントの使用に合わせてカスタマイズされた任意の文字列を指定できます。 名前をフォルダーに関連付けすると、フォルダーを検索して開くのにかかる時間が減少します。 
  

