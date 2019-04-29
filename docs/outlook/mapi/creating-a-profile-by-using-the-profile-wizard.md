---
title: プロファイルウィザードを使用してプロファイルを作成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411737"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>プロファイルウィザードを使用してプロファイルを作成する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイルウィザードは、ユーザーが最も簡単な方法でプロファイルを作成できる MAPI の機能です。 プロファイルウィザードには一連のダイアログボックスが表示され、メッセージサービスを選択して、いくつかの最も重要な構成プロパティの値を入力するようにユーザーに求めます。 その他の必要なプロパティのほとんどについて、プロファイルウィザードは提供されている既定値を使用します。 プロファイルウィザードを起動するには、 [launchwizardentry](launchwizardentry.md) prototype に基づく関数として、 **launchwizard**を呼び出します。 
  
ユーザーは、プロファイルウィザードをサポートする新しいプロファイルに、これらのメッセージサービスとサービスプロバイダーのみを追加できます。 各メッセージサービスでは、プロファイルウィザードで処理できるよりも多くのプロパティを設定する必要がある場合があるため、この方法を使用する場合は、1つ以上の選択されたサービスまたはプロバイダーが不完全に構成される可能性があることに注意してください。
  

