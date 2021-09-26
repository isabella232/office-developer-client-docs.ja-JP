---
title: プロファイル ウィザードを使用したプロファイルの作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: eed28b64effa080a604e1ea97ddf5911796e07ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631035"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a>プロファイル ウィザードを使用したプロファイルの作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロファイル ウィザードは、ユーザーが可能な限り簡単な方法でプロファイルを作成できる MAPI 機能です。 プロファイル ウィザードには、一連のダイアログ ボックスが表示され、メッセージ サービスを選択し、いくつかの最も重要な構成プロパティの値を入力するようユーザーに求めるプロンプトが表示されます。 その他の必須プロパティのほとんどで、プロファイル ウィザードは指定された既定値を使用します。 プロファイル ウィザードを呼び出す場合は、LAUNCHWIZARDENTRY プロトタイプに基づく関数 **LaunchWizard**[を呼び出](launchwizardentry.md)します。 
  
ユーザーは、プロファイル ウィザードをサポートする新しいプロファイルに、これらのメッセージ サービスとサービス プロバイダーのみを追加できます。 各メッセージ サービスでは、プロファイル ウィザードで処理できるプロパティよりも多くのプロパティを設定する必要がある場合があります。この方法を使用すると、選択したサービスまたはプロバイダーの 1 つ以上が不完全に構成される可能性があります。
  

