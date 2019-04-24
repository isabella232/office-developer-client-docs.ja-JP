---
title: Exp 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: 指定した式の指数値を戻します。
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308198"
---
# <a name="exp-function-access-custom-web-app"></a>Exp 関数 (Access カスタム web アプリ)

指定した式の指数値を戻します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Exp**(*NumericExpression*) 
  
**Exp** 関数には以下の引数が含まれます。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *NumericExpression*  <br/> |Double 型、または Double に暗黙的に変換できる式。  <br/> |
   
## <a name="remarks"></a>解説

定数 **e** (2.718281...) は、自然対数の基数です。 
  
ある数値の指数とは、定数 **e** をべき乗する数値です。たとえば、 **Exp** (1.0) = e^1.0 = 2.71828182845905 となり、 **Exp** (10) = e^10 = 22026.4657948067 となります。 
  
数値の自然対数の指数は、数値そのものを示します。 **Exp** (LOG (n)) = n。 また、数値の指数の自然対数は、数値自体: LOG (**Exp** (n)) = n となります。 
  

