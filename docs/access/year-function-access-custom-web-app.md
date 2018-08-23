---
title: Year 関数 (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: グレゴリオ暦で指定した日付の年を表す数値が返されます。
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798764"
---
# <a name="year-function-access-custom-web-app"></a>Year 関数 (カスタム web アプリケーションのアクセス)

グレゴリオ暦で指定した日付の年を表す数値が返されます。
  
> [!NOTE]
> この記事で説明されているクラウド ストレージ機能は、Office 2013 および Office 2016 ではサポートされなくなっているため、次のエラーが発生する可能性があります。 >  *申し訳ございません。サーバーで問題が発生しているため、現在 \<サービス\> を追加できません。後でもう一度お試しください。* > Office Online、Office for iOS、Office for Android のクラウド ストレージについて、[Office クラウド ストレージ パートナー プログラム](https://dev.office.com/programs/officecloudstorage)でお調べいただけます。 
  
## <a name="syntax"></a>構文

 **年**(*日付*) 
  
**Year** 関数には次の引数があります。 
  
|**引数名**|**説明**|
|:-----|:-----|
| *Date*  <br/> |日付/時刻の値に解決可能な式。 *日付*引数の式、列式、ユーザー定義変数またはリテラル文字列です。  <br/> |
   
## <a name="remarks"></a>解説

**Year** 関数、 **Month** 関数、および **Day** 関数によって返される値は、指定したデータ値の表示形式に関係なく、グレゴリオ暦の値になります。たとえば、指定したデータ値の表示形式でイスラム暦を使用する場合でも、 **Year** 関数、 **Month** 関数、および **Day** 関数で返される値は、イスラム暦に対応するグレゴリオ暦の値になります。 
  

