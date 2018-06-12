---
title: 関数 (カスタム web アプリケーションのアクセス) を選択します。
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: a6db959945bfcfc15993d3979cb9b2b3da0da904
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798574"
---
# <a name="choose-function-access-custom-web-app"></a>関数 (カスタム web アプリケーションのアクセス) を選択します。

値のリストから、指定されたインデックスの位置にあるアイテムを返します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

**選択**(*IndexNumber**値*を [*Value_n*]) 
  
**Choose** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *IndexNumber*  <br/> |この引数に続くアイテム リストのインデックス (1 から始まるインデックス) を表す整数式。  <br/> |
| *値*  <br/> |任意のデータ型の値のリスト。  <br/> |
   
## <a name="remarks"></a>注釈

指定された*IndexNumber*が整数でない場合は、値は暗黙的に整数に変換します。 
  
**インデックス値は、値の配列の境界を超えている場合 NULL が返されます。** 
  

