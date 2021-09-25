---
title: SetProperty マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: SetProperty/プロパティの設定アクションを使用して、ビュー上のコントロールのプロパティを設定できます。
ms.openlocfilehash: 1f72d038d522b9ed6e1b1c6d27dd948d8ee7352a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601493"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty マクロ アクション (Access カスタム Web アプリ)

" **SetProperty/プロパティの設定** " アクションを使用して、ビュー上のコントロールのプロパティを設定できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

"**SetField/フィールドの設定**" アクションには、以下の表に示す引数があります。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
| _コントロール名_ <br/> |プロパティ値を設定する対象のフィールドまたはコントロールの名前を指定します。ビューのプロパティを設定する場合は、この引数を指定しないでください。  <br/> |
| _プロパティ_ <br/> |設定するプロパティを選択します。このアクションを使用して設定できるプロパティの一覧については、この記事の「解説」セクションを参照してください。<br/> |
| _値_ <br/> |プロパティに対して設定する値を入力します。値が [はい] または [いいえ] のどちらかになるプロパティでは、[はい] の場合は「-1」、[いいえ] の場合は「0」を入力します。<br/> |
   
## <a name="remarks"></a>注釈

"**SetProperty/プロパティの設定**" アクションを使用して、コントロールの以下のプロパティを設定できます。 
  
- Caption
    
- Enabled
    
- ForeColor
    
- Value
    
- Visible
    
" *Value/値* " 引数に無効な値を入力すると、エラーは発生しませんが、引数がどのように解釈されるかに応じて、プロパティは別の値に変更される可能性があります。 
  

