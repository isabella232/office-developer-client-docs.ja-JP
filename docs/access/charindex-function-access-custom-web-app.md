---
title: CharIndex 関数 (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 340ed9a8-6f82-4aa8-a951-2c453b3d1ac4
description: あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
ms.openlocfilehash: dc6906f70bc5bb17e12855d69946281909962988
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282608"
---
# <a name="charindex-function-access-custom-web-app"></a>CharIndex 関数 (Access カスタム web アプリ)

あるテキスト式を他のテキスト式内で検索して、それが見つかった場合はその開始位置を戻します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**CharIndex**(*textexpression*、 *within text*、[*Start*]) 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
| *TextExpression*  <br/> |はい  <br/> |検索するテキストを含むテキスト式。  <br/> |
| *戻し*  <br/> |はい  <br/> |検索するテキスト式。  <br/> |
| *Start*  <br/> |いいえ  <br/> |検索を開始する、*テキスト*内の位置を指定する整数。 *Start*が指定されていない場合、負の数である場合、または0の場合は、検索はその*テキスト*の先頭から開始されます。  <br/> |
   
## <a name="remarks"></a>解説

If either  *TextExpression*  or  *WithinText*  is NULL,  *CharIndex*  returns NULL. 
  
*textexpression*が内部に存在し** ない場合、 *CharIndex*は0を返します。 
  
戻される開始位置は、0 ベースではなく、1 ベースです。
  

