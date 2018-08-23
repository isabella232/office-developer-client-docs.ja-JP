---
title: SetProperty マクロ アクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: SetProperty/プロパティの設定アクションを使用して、ビュー上のコントロールのプロパティを設定できます。
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798729"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>SetProperty マクロ アクション (カスタム web アプリケーションのアクセス)

" **SetProperty/プロパティの設定** " アクションを使用して、ビュー上のコントロールのプロパティを設定できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="setting"></a>設定

" **SetField/フィールドの設定** " アクションには、以下の表に示す引数があります。 
  
|**アクションの引数**|**説明**|
|:-----|:-----|
| _コントロール名_ <br/> |プロパティ値を設定する対象のフィールドまたはコントロールの名前を指定します。ビューのプロパティを設定する場合は、この引数を指定しないでください。  <br/> |
| _プロパティ_ <br/> |設定するプロパティを選択します。 このアクションを使用して設定できるプロパティの一覧については、この資料の **「解説」** セクションを参照してください。  <br/> |
| _値_ <br/> |プロパティを設定する値を入力します。 プロパティの値を持つか、[はい] またはいいえ、 **-1**を使用して、[はい] を [いいえ] は**0**  <br/> |
   
## <a name="remarks"></a>注釈

" **SetProperty/プロパティの設定** " アクションを使用して、コントロールの以下のプロパティを設定できます。 
  
- Caption
    
- Enabled
    
- ForeColor
    
- Value
    
- Visible
    
" *Value/値* " 引数に無効な値を入力すると、エラーは発生しませんが、引数がどのように解釈されるかに応じて、プロパティは別の値に変更される可能性があります。 
  

