---
title: 不一致データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 001899f7-5b1a-4c0b-a0e4-e01985eea818
description: LookupRecord データ ブロックは、特定のレコードに対して一連のアクションを実行します。
ms.openlocfilehash: 7012fecdf0e73647b2b8177473dd8b5540b5fcca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798614"
---
# <a name="lookuprecord-data-block-access-custom-web-app"></a>不一致データ ブロック (カスタム web アプリケーションのアクセス)

**LookupRecord** データ ブロックは、特定のレコードに対して一連のアクションを実行します。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> [!メモ] **LookupRecord** データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

**LookupRecord** アクションの引数は次のとおりです。 
  
|**引数**|**必須**|**説明**|
|:-----|:-----|:-----|
| _で_ <br/> |はい  <br/> |操作対象のレコードを識別する文字列です。 ** 引数は、テーブル、選択クエリ、または SQL ステートメントの名前を含めることができます。  <br/> |
| _Where Condition_ <br/> |いいえ  <br/> |**不一致**のデータ ブロックのデータの範囲を制限するために使用する文字列式を実行するとします。 抽出条件を指定する SQL 式の WHERE 句にはあります。 基準を省略すると、**不一致**のデータ ブロック*に*引数で指定されたドメイン全体で動作します。 条件に含まれる任意のフィールドは、フィールド*内*にもあります。  <br/> |
| _エイリアス_ <br/> |いいえ  <br/> |** 引数で指定されたレコードに別の名前を提供する文字列です。 あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。 *エイリアス*が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。  <br/> |
   
## <a name="remarks"></a>注釈

** *条件*引数で指定した抽出条件は、複数のレコードを指定した場合、**不一致**のデータ ブロックはに対してのみ動作の最初のレコード。 
  
レコード*条件*を満たしているないいるかどうか*に*レコードが存在しない、する場合、**不一致**は**Null**値を含むすべてのフィールドを空白のレコードを作成します。 
  

