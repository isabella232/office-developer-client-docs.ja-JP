---
title: Round 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: 指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
ms.openlocfilehash: 5a3df4a4ddd7aace5edf886db5988704e5dd6af3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798735"
---
# <a name="round-function-access-custom-web-app"></a>Round 関数 (カスタム web アプリケーションのアクセス)

指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **ラウンド**(*番号*、*有効桁数*は、[ *TruncateInsteadOfRound* ]) 
  
**Round** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Number*  <br/> |数値式を指定します。  <br/> |
| *精度*  <br/> |精度*数値*が丸められます。  *有効桁数*は、数値式である必要があります。 *精度*が正の数値の場合は、長さが指定した 10 進数の位置の数に*数値*が丸められます。 *有効桁数*に負の数がある場合は、長さの指定に従って、小数点の左側にある*数値*が丸められます。  <br/> |
| *TruncateInsteadOfRound*  <br/> |実行する操作の種類。 省略すると 0 に設定、*数値*が丸められます。 0 以外の値を指定すると、*番号*が切り捨てられます。 既定値は 0 です。  <br/> |
   
## <a name="remarks"></a>注釈

 **Round** は常に値を返します。長さが負の値であり、少数点よりも前の桁数よりも大きい場合、 **Round** は 0 を返します。 
  

