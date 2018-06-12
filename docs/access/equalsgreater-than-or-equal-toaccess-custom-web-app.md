---
title: 大きいまたは等しい (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: 2 つの式を比較して "以上" であるかどうかを判定します。
ms.openlocfilehash: 425745d8634f92e3bcce3cbfcd7d11a890e3be4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798571"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a>大きいまたは等しい (カスタム web アプリケーションのアクセス)

2 つの式を比較して "以上" であるかどうかを判定します。
  
> [!IMPORTANT]
> [!重要] マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

`>= (Greater Than or Equal To)`

*expression*  \>=  *expression* 
  
*expression*  任意の有効な式です。式は両方とも、暗黙的に変換可能なデータ型でなければなりません。変換は、データ型の優先順位のルールに依存します。 
  
## <a name="return-type"></a>戻り値の型

**ブール型 (Boolean)**
  
## <a name="remarks"></a>Remarks

NULL 以外の式を比較したときに、左側のオペランドの値が右側のオペランドの値以上の場合、結果は TRUE です。それ以外の場合、結果は FALSE です。
  

