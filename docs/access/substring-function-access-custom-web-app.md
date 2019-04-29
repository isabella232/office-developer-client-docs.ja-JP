---
title: SubString 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: 文字列式の一部が返されます。
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433473"
---
# <a name="substring-function-access-custom-web-app"></a>SubString 関数 (Access カスタム web アプリ)

文字列式の一部が返されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **SubString** (*TextExpression*, *Start*, *Length*) 
  
**SubString** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *TextExpression*  <br/> |文字列式。  <br/> |
| *Start*  <br/> |返される文字の開始位置を指定する整数式。Start が 1 未満の場合、返される式は式に指定された最初の文字から始まります。 この場合、返される文字列の数は、Start + Length - 1 または 0 のいずれか大きい方になります。開始位置が値式の文字数を超える場合は、長さゼロの式が返されます。  <br/> |
| *Length*  <br/> |返される式の文字数を指定する整数式。長さが負数の場合はエラーは生成され、ステートメントが終了します。Start と Length の合計が式の文字数を超える場合は、値式全体が先頭から返されます。  <br/> |
   

