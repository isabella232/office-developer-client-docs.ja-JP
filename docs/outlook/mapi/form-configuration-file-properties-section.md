---
title: フォーム構成ファイル [Properties] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800115"
---
# <a name="form-configuration-file-properties-section"></a>フォーム構成ファイル [Properties] セクション

  
  
**適用対象**: Outlook 
  
**[プロパティ]** セクションでフォームを使用し、公開のプロパティの完全なセットを一覧表示します。作成し、そのカスタム メッセージを MAPI クライアント アプリケーションのプロパティは、検索結果フォルダーの設定、内容のテーブルのフィルター処理、列を表示するときに使用し、ためにできます。 このプロパティ リスト内の各エントリを参照して、その後 **[プロパティ**。 _文字列_**]** のセクションに示すように次のようです。 
  
 **[のプロパティ]**
  
 **プロパティです。** _文字列_ =  _の文字列_
  
形式を [**プロパティ**。 _文字列_]セクションは次のとおりです。 
  
 **[プロパティです。** _文字列_**]**
  
 **タイプ** =  _の整数_
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _の文字列_
  
 **NmidInteger** =  _の整数_
  
 **表示名** =  _の文字列_
  
 **フラグ** =  _の整数_
  
 **SpecialType** = 0 | 1 
  
 **Enum1** =  _の文字列_
  
各 **[プロパティ**。 _文字列_**]** では、1 つのプロパティをについて説明します。 **型**指定では、MAPI プロパティの種類、たとえば 3 (PT_I4)、プロパティを使用します。 **NmidPropset**エントリは省略可能です。**NmidString**エントリまたは**NmidInteger**エントリのいずれかとは、 **NmidPropset**のエントリは、プロパティの名前を示します。 **NmidInteger**プロパティの識別子を使用するときに、 **NmidString**は、プロパティの名前を示します。 **NmidString**と**NmidInteger**は、相互に排他的です。 
  
セット、 **NmidPropset**には、プロパティ セットの名前が含まれている必要がある場合省略すると、 **NmidPropset**は、次のルールに基づいて既定値に設定されている場合: **NmidInteger**が存在し、その値が 0x8000 未満である場合**NmidPropset**が PS_MAPI に設定されています。 **NmidInteger**の値が整数値 0x8000 に割り当てより大きい値に設定されている場合、またはそれが存在しない場合は、 **NmidPropset**が PS_PUBLIC_STRINGS に設定されています。 
  
**表示名**のエントリには、プロパティのラベルが含まれています。 **SpecialType**エントリが存在し、0 以外の場合は、このプロパティは、特殊なプロパティであることを示します。 現時点で定義されている唯一の特別なプロパティの型は、 **SpecialType** = 1 は、列挙された文字列のプロパティを示します。 **Enum1**エントリを参照して**SpecialType**は、1 に設定されている場合、 **[Enum1 です**。 _文字列_**]** のセクションです。 
  
以下は、 **[プロパティ]** セクションの例と、 **[のプロパティ**。 _文字列_**]** のセクションです。 
  
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

上記の例への参照、それ以降の**Enum1**エントリ **[Enum1 です**。 _文字列_**]** セクションの特定の種類の列挙体を記述します。 このような列挙体の最初のプロパティに関連付ける、 **[プロパティ**。 _文字列_**]** のセクションでは、整数型のプロパティにインデックスが呼び出されます。 このような列挙体には、表示インデックスのペアを引き受けることが可能な値の一覧も含まれています。 定義によって**Enum1**エントリは、常に PT_I4 種類がいるために、列挙型のプロパティの種類を指定する必要はありません。 形式、 **[Enum1 です**。 _文字列_**]** のセクションでは。 
  
 **[Enum1。** _文字列_**]**
  
 **NmidPropset** =  _guid_
  
 **NmidString** =  _の文字列_
  
 **NmidInteger** =  _の整数_
  
 **EnumCount** =  _の整数_
  
 **Val 関数です。** _整数_**.表示** =  _の文字列_
  
 **Val 関数です。** _整数_**.インデックス** =  _の整数_
  
火災の危険を低、中、高の値を持つ名前付き列挙型のプロパティのプロパティの定義例を次に示します。
  
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

 **[Enum1。** _文字列_**]** のセクションでは、2 つの目的のアプリケーションで使用することができます: 文字列の代わりに、インデックスを使用して、プロパティのフィルター処理を高速化し、文字列値のアルファベット順とは異なる順序で並べ替えるには。 たとえば、並べ替え行います高-低の順序ではなく、低、中、高順に基づいて。 
  

