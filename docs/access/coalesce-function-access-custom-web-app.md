---
title: Coalesce 関数 (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: 一連の引数から Null でない最初の式を返します。
ms.openlocfilehash: e3b238c2aa407a45893cb85ecf3d6867e7f6082f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581708"
---
# <a name="coalesce-function-access-custom-web-app"></a>Coalesce 関数 (Access カスタム Web アプリ)

一連の引数から Null でない最初の式を返します。
  
> [!NOTE]
> この記事で説明するクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなったので、> 申し訳ありませんが、サーバーの問題が発生するため、今は追加できません。 *\<service\>後でやり直してください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについては、Office Cloud Storage パートナー プログラムを[参照してください](https://dev.office.com/programs/officecloudstorage)。 
  
## <a name="syntax"></a>構文

**Coalesce** (Value **, [Value **], …,[Value **]) 
  
**Coalesce** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *値*  <br/> |式。  <br/> |
   
## <a name="remarks"></a>注釈

すべての引数が NULL の場合、**Coalesce** は NULL を返します。 
  
## <a name="example"></a>例

次の式をテーブルの入力規則として使用します。この式は、レコードを確定する前に、First Name、Last Name, Email、Mobile Phone、Work Phone、Home Phone、および Company の各フィールドの入力を確認します。これらのどのフィールドも空で残されている場合、**Coalesce** 関数は NULL を返します。これは、入力規則の違反です。 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


