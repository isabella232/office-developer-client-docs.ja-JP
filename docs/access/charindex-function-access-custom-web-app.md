---
title: CharIndex 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: bd0b14210a4e4ac73cbbca6198fa86d823853f88
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577718"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex 関数 (Access カスタム Web アプリ)

あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**CharIndex** (*TextExpression*, *WithinText*, [*Start*]) 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |必要  <br/> |検索するテキストを含むテキスト式。  <br/> |
| *WithinText*  <br/> |必要  <br/> |検索するテキスト式。  <br/> |
| *Start*  <br/> |いいえ  <br/> |検索を開始する  *WithinText*  の場所を指定する整数。 Start  *が*  指定されていない場合、負の数値、または 0 の場合、検索は WithinText の先頭から  *始まります*  。  <br/> |
   
## <a name="remarks"></a>注釈

If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL. 
  
*WithinText 内に TextExpression* *が見つからない* 場合 *、CharIndex* は 0 を返します。 
  
戻される開始位置は、0 ベースではなく、1 ベースです。
  

