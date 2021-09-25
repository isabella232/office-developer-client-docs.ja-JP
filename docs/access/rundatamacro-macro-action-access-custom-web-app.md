---
title: RunDataMacro マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: f6010ac5-6c08-4c1b-a811-ff81b30ed5f0
description: RunDataMacro/データマクロの実行アクションを使用して、スタンドアロンデータ マクロを実行できます。
ms.openlocfilehash: 4505bf5eadda4cf0c12af73b050826b6493be139
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580602"
---
# <a name="rundatamacro-macro-action-access-custom-web-app"></a>RunDataMacro マクロ アクション (Access カスタム Web アプリ)

" **RunDataMacro/データマクロの実行** " アクションを使用して、スタンドアロンデータ マクロを実行できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

"RunDataMacro/データマクロの実行" アクションの引数は次のとおりです。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
| _Macro Name/マクロ名_ <br/> |実行するデータ マクロの名前  <br/> |
   
## <a name="remarks"></a>注釈

マクロ デザイナーで実行するデータ マクロを選択すると、そのデータ マクロにパラメーターが必要であるかどうかが自動的に判断されます。パラメーターが必要な場合は、引数を入力するテキストボックスが表示されます。
  
When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro. When the called data macro has finished, Access returns to the original macro and runs the next action. 
  

