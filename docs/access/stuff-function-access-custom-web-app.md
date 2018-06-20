---
title: Stuff 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798740"
---
# <a name="stuff-function-access-custom-web-app"></a>Stuff 関数 (カスタム web アプリケーションのアクセス)

テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **もの**(*IntoTextExpression*、*開始*、*長さ*、 *ThisTextExpression*) 
  
**Stuff** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |*ThisTextExpression*で指定されたテキストを挿入するテキストを指定する文字列式を指定します。  <br/> |
| *Start*  <br/> |削除と挿入を開始する場所を指定する整数値です。 開始または長さが負の場合は、null 文字列が返されます。 Start が最初の*IntoTextExpression*よりも長い場合は、null 文字列が返されます。  <br/> |
| *Length*  <br/> |削除する文字の数を指定する整数です。 長さが最初の*IntoTextExpression*よりも長い場合は、最後の*IntoTextExpression*の最後の文字まで削除が発生します。  <br/> |
| *ThisTextExpression*  <br/> |テキスト式のハットは、 *IntoTextExpression*に挿入するテキストを指定します。 この式は、*開始*時の*IntoTextExpression*の先頭文字に置き換えられます。  <br/> |
   
## <a name="remarks"></a>注釈

*開始*または*長*の引数が負の場合、開始位置が 1 番目の文字列の長さよりも大きい場合や、null 文字列が返されます。 開始位置が 0 の場合は、null 値が返されます。 削除する長さが 1 番目の文字列より長い場合は、最初の文字列の最初の文字まで削除されます。 
  

