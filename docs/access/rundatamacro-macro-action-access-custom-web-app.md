---
title: RunDataMacro マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: RunDataMacro/データマクロの実行アクションを使用して、スタンドアロンデータ マクロを実行できます。
ms.openlocfilehash: 55a0ff4c731dc517c5d71aa20d8e46c3b4ff4611
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798726"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>RunDataMacro マクロ アクション (カスタム web アプリケーションのアクセス)

" **RunDataMacro/データマクロの実行** " アクションを使用して、スタンドアロンデータ マクロを実行できます。 
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

" **RunDataMacro/データマクロの実行** " アクションの引数は次のとおりです。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
| _Macro Name/マクロ名_ <br/> |実行するデータ マクロの名前  <br/> |
   
## <a name="remarks"></a>解説

マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。
  
**RunDataMacro**アクションを含むマクロを実行するし、 **RunDataMacro**アクションに到達して、data という名前のマクロが実行されます。 Data という名前のマクロが完了したら、アクセスが元に戻りし、次のアクションを実行します。 
  

