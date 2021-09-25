---
title: フォーム構成ファイル [プロパティ] セクション
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fa32c4145292769951500b43f2684b6602552a1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576255"
---
# <a name="form-configuration-file-properties-section"></a>フォーム構成ファイル [プロパティ] セクション

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[ **プロパティ] セクションには** 、フォームが使用して発行するプロパティの完全なセットが一覧表示されます。つまり、MAPI クライアント アプリケーションが列の表示、コンテンツ テーブルのフィルター処理、検索結果フォルダーの設定時に使用できるカスタム メッセージで作成するプロパティです。 このプロパティ リスト内の各エントリは、後続の **[プロパティ] を参照します。** _次に_**示すように**、string ] セクションを使用します。 
  
 **[プロパティ]**
  
 **プロパティ。** _string_  =  _string_
  
[ プロパティ] の **形式を指定します。** _string_]セクションは次の場合です。 
  
 **[プロパティ]** _string_ **]**
  
 **型**  =  _integer_
  
 **NmidPropset**  =  _guid_
  
 **NmidString**  =  _string_
  
 **NmidInteger**  =  _integer_
  
 **DisplayName**  =  _string_
  
 **フラグ**  =  _integer_
  
 **SpecialType** = 0|1 
  
 **Enum1**  =  _string_
  
各 **[プロパティ]** _string_ **] セクション** では、1 つのプロパティについて説明します。 Type **エントリ** は、プロパティの MAPI プロパティの種類 (たとえば、3 (PT_I4) を指定します。 **NmidPropset エントリ** はオプションです。NmidString エントリまたは **NmidInteger** エントリと共に **、NmidPropset** エントリはプロパティの名前を指定します。  **NmidString** はプロパティの名前を指定し **、NmidInteger はプロパティ** の識別子を指定します。 **NmidString と** **NmidInteger は** 相互に排他的です。 
  
設定されている場合 **、NmidPropset には** プロパティ セットの名前が含まれている必要があります。指定しない場合 **、NmidPropset** は次のルールに基づいて既定値に設定されます **。NmidInteger** が存在し、その値が 0x8000 未満の場合 **、NmidPropset** は PS_MAPI に設定されます。 **NmidInteger** の値が 0x8000 より大きい整数に設定されている場合、または指定しない場合 **、NmidPropset** は PS_PUBLIC_STRINGS に設定されます。 
  
**DisplayName エントリ** には、プロパティのラベルが含まれる。 **SpecialType エントリ**(存在する場合と 0 以外の場合) は、このプロパティが特別なプロパティを示します。 現在、定義されている特殊なプロパティの種類は **SpecialType** = 1 のみです。これは文字列列挙プロパティを示します。 **SpecialType が** 1 に設定されている場合 **、Enum1** エントリは **[Enum1] を参照します。** _string_ **]** セクション。 
  
[プロパティ] セクションと **[プロパティ]** の例を **次に示します。** _string_ **]** セクション。 
  
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

前 **出の例の Enum1** エントリは、後続の **[Enum1] を参照します。** _string_ **] セクション** で、特定の型の列挙を説明します。 このような列挙体は、[プロパティ] の最初のプロパティ **を関連付けます。** _string_ **]** セクションに、インデックスと呼ばれる整数プロパティを指定します。 このような列挙には、表示インデックスペアが想定できる値の一覧も含まれます。 列挙体のプロパティの種類を指定する必要は不要です。定義上 **、Enum1** エントリには常に列挙型PT_I4があります。 **[Enum1] の形式を指定します。** _string_ **] セクション** は次の場合です。 
  
 **[Enum1.** _string_ **]**
  
 **NmidPropset**  =  _guid_
  
 **NmidString**  =  _string_
  
 **NmidInteger**  =  _integer_
  
 **EnumCount**  =  _integer_
  
 **Val。** _integer_ **.表示**  =   _文字列_
  
 **Val。** _integer_ **.インデックス**  =   _の整数_
  
次に示すのは、低、中、高の値を指定できる Fire Hazard という名前の列挙プロパティのプロパティ定義の例です。
  
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

 **[Enum1.** _string_ **] セクション** は、アプリケーションで、文字列の代わりにインデックスを使用してプロパティのフィルター処理を高速化し、文字列値の英数字の順序とは異なる順序で並べ替えるという 2 つの目的で使用できます。 たとえば、並べ替えは、高中低の順序ではなく、低中高の順序に基づいて実行できます。 
  

