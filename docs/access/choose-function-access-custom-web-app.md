---
title: 関数の選択 (カスタム Web アプリへのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: 3b2ce27b0bd43c2db1d28f90a0ffbd5c2c206496
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573335"
---
# <a name="choose-function-access-custom-web-app"></a>関数の選択 (カスタム Web アプリへのアクセス)

値のリストから、指定されたインデックスの位置にあるアイテムを返します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**Choose** (*IndexNumber*, *Value*,*[* Value_n ]) 
  
**Choose** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *IndexNumber*  <br/> |この引数に続くアイテム リストのインデックス (1 から始まるインデックス) を表す整数式。  <br/> |
| *値*  <br/> |任意のデータ型の値のリスト。  <br/> |
   
## <a name="remarks"></a>注釈

If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer. 
  
インデックス値が値の配列の境界を超えた場合 **、Choose** は NULL を返します。 
  

