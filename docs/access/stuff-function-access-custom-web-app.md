---
title: Stuff 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
ms.openlocfilehash: f062ae87982b0c3811891b1fa9df777123c7478d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593048"
---
# <a name="stuff-function-access-custom-web-app"></a>Stuff 関数 (Access カスタム Web アプリ)

テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Stuff** (IntoTextExpression **, Start **, Length **, ThisTextExpression **) 
  
**Stuff** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *IntoTextExpression*  <br/> |*ThisTextExpression* で指定されたテキストを挿入するテキストを指定するテキスト式。  <br/> |
| *Start*  <br/> |削除および挿入の開始位置を指定する整数値。 開始位置または長さが負の値の場合、null 文字列が返されます。 start が最初の  *IntoTextExpression*  より長い場合は、null 文字列が返されます。  <br/> |
| *Length*  <br/> |削除する文字数を指定する整数。 長さが最初の  *IntoTextExpression*  より長い場合、最後の  *IntoTextExpression*  の最後の文字まで削除が行われます。  <br/> |
| *ThisTextExpression*  <br/> |テキスト式のハットは  *、IntoTextExpression に挿入するテキストを指定します*  。 この式は、Start で始まる *IntoTextExpression の* 長さ文字を置き換 *える。*  <br/> |
   
## <a name="remarks"></a>注釈

If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned. If the start position is 0, a null value is returned. If the length to delete is longer than the first string, it is deleted to the first character in the first string. 
  

