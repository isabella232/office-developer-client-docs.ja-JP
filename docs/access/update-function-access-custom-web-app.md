---
title: 更新関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: 指定したフィールドの挿入または更新操作が試行されたかどうかを返します。
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798767"
---
# <a name="update-function-access-custom-web-app"></a>更新関数 (カスタム web アプリケーションのアクセス)

指定したフィールドの挿入または更新操作が試行されたかどうかを返します。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **更新**(*列*) 
  
**更新**関数には、次の引数が含まれています。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Column*  <br/> |INSERT または UPDATE 操作をチェックするフィールドの名前。  <br/> |
   
## <a name="remarks"></a>注釈

**更新**関数は、挿入または更新の試行が成功したかどうかに関係なく、TRUE を返します。 
  

