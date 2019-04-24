---
title: Round 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: 指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307960"
---
# <a name="round-function-access-custom-web-app"></a>Round 関数 (Access カスタム web アプリ)

指定された長さまたは精度で四捨五入されたか切り捨てられた数値を返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Round**(*数値*、*精度*、[ *TruncateInsteadOfRound* ]) 
  
**Round** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Number*  <br/> |数式。  <br/> |
| *精度*  <br/> |丸められる桁数** を指定します。  *精度*は、数値式である必要があります。 *精度*に正の数値を指定すると、引数*number*は引数 length で指定した小数点の桁数に四捨五入されます。 *精度*に負の数値を指定すると、引数 length で指定した*数値*が小数点の左側で四捨五入されます。  <br/> |
| *TruncateInsteadOfRound*  <br/> |実行する操作の種類。 省略するか0に設定すると、*数値*は丸められます。 0以外の値を指定すると、*数値*は切り捨てられます。 既定値は 0 です。  <br/> |
   
## <a name="remarks"></a>解説

 **Round** は常に値を返します。長さが負の値であり、少数点よりも前の桁数よりも大きい場合、 **Round** は 0 を返します。 
  

