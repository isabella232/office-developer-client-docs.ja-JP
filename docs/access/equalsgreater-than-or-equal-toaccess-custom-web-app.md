---
title: 以上 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: cceb8dcb-5ce1-4c32-b057-6201b62a646f
description: 2 つの式を比較して、"以上" かどうかを判定します。
localization_priority: Priority
ms.openlocfilehash: 76472544be950c68f3b5d42fe13b3040e9268f48
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709258"
---
# <a name="greater-than-or-equal-to-access-custom-web-app"></a>以上 (Access カスタム Web アプリ)

2 つの式を比較して、"以上" かどうかを判定します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-JP/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

`>= (Greater Than or Equal To)`

*expression*  \>=  *expression* 
  
*expression*  任意の有効な式です。式は両方とも、暗黙的に変換可能なデータ型でなければなりません。変換は、データ型の優先順位のルールに依存します。 
  
## <a name="return-type"></a>戻り値の型

**Boolean**
  
## <a name="remarks"></a>解説

NULL 以外の式を比較したときに、左側のオペランドの値が右側のオペランドの値以上の場合、結果は TRUE です。それ以外の場合、結果は FALSE です。
  

