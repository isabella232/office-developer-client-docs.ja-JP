---
title: Concat 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 38ad6365-79df-4342-9b76-ca27b8ab8952
description: 複数の文字列値を結合した結果の文字列を戻します。
ms.openlocfilehash: fc0de43e5e42cc1c39ee89cf76058b8039daf279
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798548"
---
# <a name="concat-function-access-custom-web-app"></a>Concat 関数 (カスタム web アプリケーションのアクセス)

複数の文字列値を結合した結果の文字列を戻します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**連結**(*値 1**値 2*、.[*ValueN*]) 
  
**Concat** 関数には、以下の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
|値  <br/> |その他の値に連結する文字列値。  <br/> |
   
## <a name="remarks"></a>注釈

**Concat** は複数の文字列引数を単一の文字列に連結します。少なくとも 2 つの文字列引数が必要です。文字列引数が 1 つの場合は、エラーが発生します。 
  
すべての引数は文字列データ型に暗黙的に変換されてから、連結されます。
  
## <a name="example"></a>例

テーブルに FirstName、MiddleInitial、および LastName の各フィールドが含まれる場合、次の式を使用して人のフル ネームを表示できます。 ミドル ネームのイニシャル] フィールドが空白の場合は、完全な名前を表示する] フィールドと [姓] フィールドのみが結合されます。
  
```vb
IIf([MiddleInitial] Is Null,Concat([FirstName]," ",[LastName]),Concat([FirstName]," ",[MiddleInitial]," ",[LastName]))
```


