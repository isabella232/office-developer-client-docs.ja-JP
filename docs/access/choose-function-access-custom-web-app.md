---
title: 関数の選択 (カスタム Web アプリへのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: 値のリストから、指定されたインデックスの位置にあるアイテムを返します。
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414117"
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
  

