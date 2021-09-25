---
title: Round 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: 指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
ms.openlocfilehash: e974cecbc2f602af12ba7aa572541c2f9bee319f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593069"
---
# <a name="round-function-access-custom-web-app"></a>Round 関数 (Access カスタム Web アプリ)

指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ]) 
  
**Round** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Number*  <br/> |数式。  <br/> |
| *精度*  <br/> |数値を四捨  *五入*  する精度。  *精度*  は、数値式である必要があります。 Precision  *が*  正の数値の場合  *、Number*  は長さによって指定された小数点以下の桁数に丸められます。 Precision  *が*  負の数値の場合  *、Number*  は長さによって指定された小数点の左側に四捨五入されます。  <br/> |
| *TruncateInsteadOfRound*  <br/> |実行する操作の種類。 省略または 0 に設定すると、  *数値は四捨*  五入されます。 0 以外の値を指定すると  *、Number*  は切り捨てされます。 既定値は 0 です。  <br/> |
   
## <a name="remarks"></a>注釈

 **Round** は常に値を返します。長さが負の値であり、少数点よりも前の桁数よりも大きい場合、 **Round** は 0 を返します。 
  

