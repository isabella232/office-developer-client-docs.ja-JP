---
title: ユーザー関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427676"
---
# <a name="stuff-function-access-custom-web-app"></a>ユーザー関数 (Access カスタム web アプリ)

テキスト文字列を別のテキスト文字列に挿入します。1 番目の文字列の開始位置から、指定された長さの文字が削除され、1 番目の文字列の開始位置に 2 番目の文字列が挿入されます。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **Stuff** (IntoTextExpression**, Start**, Length**, ThisTextExpression**) 
  
**Stuff** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *in-extexpression*  <br/> |*ThisTextExpression*によって指定されたテキストを挿入するテキストを指定するテキスト式を指定します。  <br/> |
| *Start*  <br/> |削除および挿入の開始位置を指定する整数値。 開始位置または長さが負の値の場合、null 文字列が返されます。 start が最初の inを超える** 場合は、null 文字列が返されます。  <br/> |
| *Length*  <br/> |削除する文字数を指定する整数。 length が最初の*inの inext式*よりも長い場合、削除は最後の*in、式*の最後の文字まで行われます。  <br/> |
| *ThisTextExpression*  <br/> |テキスト式 hat は、inに挿入するテキスト** を指定します。 この式は、*開始*時から始まる*inserviceprovider extexpression*の長さ文字を置き換えます。  <br/> |
   
## <a name="remarks"></a>注釈

If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned. If the start position is 0, a null value is returned. If the length to delete is longer than the first string, it is deleted to the first character in the first string. 
  

