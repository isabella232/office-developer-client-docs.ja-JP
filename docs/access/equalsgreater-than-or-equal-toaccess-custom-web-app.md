---
title: 以上 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: 2 つの式を比較して、"以上" かどうかを判定します。
ms.localizationpriority: high
ms.openlocfilehash: e72991960d1b4ff5d6ac9dcecb17f50bf98871b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614865"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a>以上 (Access カスタム Web アプリ)

2 つの式を比較して、"以上" かどうかを判定します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

`>= (Greater Than or Equal To)`

*expression*  \>=  *expression* 
  
*expression*  任意の有効な式です。式は両方とも、暗黙的に変換可能なデータ型でなければなりません。変換は、データ型の優先順位のルールに依存します。 
  
## <a name="return-type"></a>戻り値の型

**ブール型 (Boolean)**
  
## <a name="remarks"></a>注釈

NULL 以外の式を比較したときに、左側のオペランドの値が右側のオペランドの値以上の場合、結果は TRUE です。それ以外の場合、結果は FALSE です。
  

