---
title: CharIndex 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: 86a46f57c64028530217326127eece887127c4c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798591"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex 関数 (カスタム web アプリケーションのアクセス)

あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**CharIndex**(*TextExpression*、 *WithinText*、[*開始*]) 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |はい  <br/> |検索するテキストを含むテキスト式。  <br/> |
| *WithinText*  <br/> |はい  <br/> |検索するテキスト式。  <br/> |
| *Start*  <br/> |いいえ  <br/> |検索を開始するのには*WithinText*の位置を指定する整数。 *開始*が指定されていないが、負の値または 0 である場合は、 *WithinText*の先頭に、検索が開始されます。  <br/> |
   
## <a name="remarks"></a>注釈

*TextExpression*または*WithinText*のいずれかが NULL の場合、 *CharIndex*は NULL を返します。 
  
*WithinText*内で*TextExpression*が見つからない場合、 *CharIndex*は 0 を返します。 
  
戻される開始位置は、0 ベースではなく、1 ベースです。
  

