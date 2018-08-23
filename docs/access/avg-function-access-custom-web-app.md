---
title: Avg 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: 指定したフィールドにある値の集合の平均値を計算します。
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798569"
---
# <a name="avg-function-access-custom-web-app"></a>Avg 関数 (カスタム web アプリケーションのアクセス)

指定したフィールドにある値の集合の平均値を計算します。
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
## <a name="syntax"></a>構文

 **平均**(*数式*) 
  
**Avg** 関数には、以下の引数があります。 
  
|**引数**|**説明**|
|:-----|:-----|
|数式  <br/> |平均値、またはそのフィールドのデータを使用して計算を実行する式にする数値データを含むフィールドを識別する文字列式です。 *数式*内のオペランドには、テーブルのフィールド、変数、または関数 (組み込みまたはユーザー定義することができますが、他の SQL 集計関数のいずれかのない) の名前を含めることができます。  <br/> |
   
## <a name="remarks"></a>解説

**Avg** 関数で計算される平均は、値の合計を値の個数で割った算術平均です。たとえば、平均運送料などを計算する場合に、 **Avg** 関数を使用します。 
  
**Avg** 関数は **Null** 値を除外して計算します。 
  

