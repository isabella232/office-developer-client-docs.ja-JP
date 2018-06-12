---
title: 関数 (カスタム web アプリケーションのアクセス) を結合します。
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: 一連の引数から Null でない最初の式を返します。
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798578"
---
# <a name="coalesce-function-access-custom-web-app"></a>関数 (カスタム web アプリケーションのアクセス) を結合します。

一連の引数から Null でない最初の式を返します。
  
> [!NOTE]
> [!メモ] この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>Syntax

**合体**(*値*、[*値*]、[*値*]) 
  
**Coalesce** 関数の引数は次のとおりです。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Value*  <br/> |式。  <br/> |
   
## <a name="remarks"></a>注釈

すべての引数が NULL の場合、 **Coalesce** は NULL を返します。 
  
## <a name="example"></a>例

次の式をテーブルの入力規則として使用します。この式は、レコードを確定する前に、First Name、Last Name, Email、Mobile Phone、Work Phone、Home Phone、および Company の各フィールドの入力を確認します。これらのどのフィールドも空で残されている場合、 **Coalesce** 関数は NULL を返します。これは、入力規則の違反です。 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


