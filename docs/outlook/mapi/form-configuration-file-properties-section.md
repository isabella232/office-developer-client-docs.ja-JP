---
title: フォーム構成ファイル [Properties] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421292"
---
# <a name="form-configuration-file-properties-section"></a>フォーム構成ファイル [Properties] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**[properties]** セクションには、フォームが使用および発行するプロパティの完全なセットがリストされています。これは、MAPI クライアントアプリケーションが列の表示、コンテンツテーブルのフィルター処理、検索結果フォルダーの設定を行うときに使用できる、カスタムメッセージ内に作成されるプロパティです。 このプロパティリストの各エントリは、後続の **[プロパティを参照します。** _文字列_**]** セクションは次のようになります。 
  
 **プロパティ**
  
 **プロパティ.** _文字列_ =  _文字列_
  
[プロパティ] の形式 **。** _string_]セクションは次のとおりです。 
  
 **プロパティ.** _文字列_**]**
  
 **** =  _整数_型
  
 **NmidPropset** =  _guid_
  
 **nmidstring** =  _文字列_
  
 **nmidinteger** =  _整数_
  
 **DisplayName** =  _文字列_
  
 **Flags** =  _整数_
  
 特別の**種類**= 0 | 1 
  
 **Enum1** =  _文字列_
  
各 **[Property.** _文字列_**]** セクションでは、1つのプロパティについて説明します。 **type**エントリは、プロパティの MAPI プロパティの種類 (例: 3 (PT_I4)) を指定します。 **NmidPropset**エントリは省略可能です。**nmidstring**エントリまたは**nmidstring**エントリのいずれかと共に、 **NmidPropset**エントリはプロパティの名前を指定します。 **nmidstring**はプロパティの名前を指定し、 **nmidstring**はプロパティの識別子を示します。 **nmidstring**と**nmidstring**は相互に排他的です。 
  
設定されている場合、 **NmidPropset**にはプロパティセットの名前を指定する必要があります。存在しない場合、 **NmidPropset**は次のルールに基づいて既定値に設定されます。 **nmidinteger**が存在し、その値が0x8000 未満の場合、 **NmidPropset**は PS_MAPI に設定されます。 **nmidinteger**の値が0x8000 を超える整数に設定されている場合、または存在しない場合、 **NmidPropset**は PS_PUBLIC_STRINGS に設定されます。 
  
**DisplayName**エントリには、プロパティのラベルが含まれています。 特別な**種類**のエントリ (存在する場合)、非ゼロの場合は、このプロパティが特別なプロパティであることを示します。 現時点では、唯一定義されている**** 特別なプロパティの型は、文字列列挙型のプロパティを示す、指定された特別なプロパティの種類です。 特別な**type**が1に設定されている場合、 **Enum1**エントリは [Enum1] を参照し**ます。** _文字列_**]** セクション 
  
**[properties]** セクションと [properties] の例を次に示し**ます。** _文字列_**]** セクション 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

前の例の**Enum1**エントリは、以降の [Enum1 を参照し**ます。** _文字列_**]** を参照してください。 このような列挙は、[property の最初のプロパティを関連付け**ます。** _文字列_**]** セクションで、インデックスと呼ばれる整数のプロパティを使用します。 この列挙型には、表示インデックスのペアが想定できる値の一覧も含まれています。 **Enum1**エントリには常に PT_I4 型が指定されているため、列挙のプロパティの種類を指定する必要はありません。 **[Enum1**の形式。 _文字列_**]** セクションは次のとおりです。 
  
 **[Enum1** _文字列_**]**
  
 **NmidPropset** =  _guid_
  
 **nmidstring** =  _文字列_
  
 **nmidinteger** =  _整数_
  
 **enumcount** =  _整数_
  
 **long.** _整数型_**.表示** =  _文字列_
  
 **long.** _整数型_**.インデックス** =  _整数_
  
次に示すのは、低、中、高の可能な値を持つ、"Fire 危険" という名前の列挙プロパティのプロパティ定義の例です。
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 **[Enum1** _文字列_**]** セクションは、次の2つの目的でアプリケーションによって使用されます。プロパティのフィルター処理を高速化するには、文字列の代わりにインデックスを使用し、文字列値のアルファベット順とは異なる順序で並べ替えます。 たとえば、高-中-低の順序ではなく、低中-高の順序に基づいて並べ替えを行うことができます。 
  

