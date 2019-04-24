---
title: フォルダーフィールドストリームの構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336891"
---
# <a name="folder-fields-stream-structures"></a>フォルダーフィールドストリームの構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの[PidTagUserFields](pidtaguserfields-canonical-property.md)プロパティには、ユーザー定義フィールド定義のフォルダーが含まれているバイナリストリーム、folderuserfields が含まれています。 このトピックでは、フォルダーのユーザー定義フィールド定義のストリーム構造について説明します。 

folderuserfields ストリーム構造は、folderuserfields dsa 構造または folderuserfields の dsa 構造のいずれかで構成され、その後に folderuserfields w 構造が続きます。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に格納されます。
  
- **folderuserフィールド ansi**: folderuserな dsa ストリーム構造。
    
- **folderuserフィールド unicode**(オプション): folderuserフィールド w stream 構造。
    
folderuserfields unicode が存在するかどうかは、folderuserfields ansi の長さを超える、folderuserfield の長さの合計によって検出されます。
  
> [!IMPORTANT]
> folderuserフィールド ansi は、古い、unicode 以外のバージョンの MAPI クライアントとの互換性を保つために使用されるため、folderuserフィールド Unicode が存在する場合、folderuserフィールド ansi の内容は無視されます。 ANSI 変換でのデータ損失を回避するために、folderuserfields ストリームを作成する場合、常に folderuserfields w パーツが含まれています。 
  
## <a name="folderuserfieldsa-stream-structure"></a>folderuseron dsa ストリーム構造

folderuseron dsa ストリーム構造は、folderuserfields 構造の folderuserfields w 部分でオーバーライドされない限り、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む、folderuserfieldsa 配列です。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に、リトルエンディアンバイト順に格納されます。
  
- **fielddefinitioncount**: このストリーム内のフィールド定義の数である DWORD (4 バイト)。 これは、 **fielddefinitions**配列内の要素の数です。
    
- **fielddefinitions**: folderfielddefinitiona stream 構造体の配列。 この配列の数は、 **fielddefinitioncount** data 要素と同じです。
    
この folderuserfieldsa が folderuserfields 構造の folderuserfields w 部分でオーバーライドされていない限り、 **fielddefinitions**配列は、最後の folderuserfieldsa の FieldType フィールドを同じにすることで、"null で終了" している必要があります。ftnull になります。
  
## <a name="folderuserfieldsw-stream-structure"></a>folderuserフィールド w Stream 構造

folderuserfields w stream 構造は、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む folderuserfieldsw stream 構造体の配列です。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に、リトルエンディアンバイト順に格納されます。
  
- **fielddefinitioncount**: このストリーム内のフィールド定義の数である DWORD (4 バイト)。 これは、 **fielddefinitions**配列内の要素の数です。
    
- **fielddefinitions**: folderfielddefinitionw ストリーム構造の配列。 この配列の数は、 **fielddefinitioncount** data 要素と同じです。
    
**fielddefinitions**配列は、最後の folderfielddefinitionw 要素の FieldType フィールドが ftnull と同じになるように "null で終了" になる必要があります。
  
## <a name="folderfielddefinitiona-stream-structure"></a>folderfielddefinitiona 構造体

folderfielddefinitiona 構造体には、ANSI に格納されているフィールド名を持つユーザー定義フィールドの定義が含まれています。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に、リトルエンディアンバイト順に格納されます。
  
- **FieldType**: fldtype (4 バイト) (このフィールドの型)。
    
- **FieldNameLength**: WORD (2 バイト)、 **FieldName**配列内の要素の数。
    
- **FieldName**: CHAR の配列。 これは、フィールド名を表す ANSI CP_ACP コードページの表現です。 この配列の数は、 **FieldNameLength**と同じです。 フィールド名は、 [UserProperties](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx)メソッドで指定されているように、name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > 以前のバージョンとの互換性を保つために、Outlook では、これらの制限に該当しないいくつかの**フィールド名**値を処理することができますが、このような場合についてはこのトピックでは説明しません。 
  
- **common**: folderfielddefinitioncommon stream 構造。
    
## <a name="folderfielddefinitionw-stream-structure"></a>folderfielddefinitionw Stream 構造

folderfielddefinitionw stream 構造には、Unicode に格納されているフィールド名を持つユーザー定義フィールドの定義が含まれています。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に、リトルエンディアンバイト順に格納されます。
  
- **FieldType**: fldtype (4 バイト) (このフィールドの型)。
    
- **FieldNameLength**: WORD (2 バイト)、 **FieldName**配列内の要素の数。
    
- **FieldName**: WCHAR の配列。 これは、フィールド名の Unicode (utf-16) 表現です。 この配列の数は、 **FieldNameLength**と同じです。 フィールド名は、 [UserProperties](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx)メソッドで指定されているように、name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > 以前のバージョンとの互換性を保つために、Outlook では、これらの制限に該当しないいくつかの**フィールド名**値を処理することができますが、そのような場合にはこのトピックでは説明しません。 
  
- **common**: folderfielddefinitioncommon stream 構造。
    
## <a name="fldtype-enumeration"></a>fldtype 列挙

次の表に、 **fldtype**列挙値を一覧表示します。 
  
|名前|値|意味|
|:-----|:-----|:-----|
|ftnull  <br/> |0x0  <br/> |このフィールド型は、フィールド定義の配列を null で終了するために使用されます。  <br/> |
|ftstring  <br/> |0x1  <br/> |テキスト  <br/> |
|ftinteger  <br/> |0x3  <br/> |整数  <br/> |
|fttime  <br/> |0x5  <br/> |日付/時刻  <br/> |
|ftboolean  <br/> |0x6  <br/> |Yes/No  <br/> |
|ftduration  <br/> |0x7  <br/> |期間  <br/> |
|ftmultistring  <br/> |0xB  <br/> |キーワード  <br/> |
|ftfloat  <br/> |0xC  <br/> |数値またはパーセント  <br/> |
|ftcurrency  <br/> |0xe  <br/> |通貨  <br/> |
|ftcalc  <br/> |0x12  <br/> |Formula  <br/> |
|ftswitch  <br/> |0x13  <br/> |最初の空ではないフィールドのみを示す型の組み合わせ。これ以降のフィールドは無視されます。  <br/> |
|ftconcat  <br/> |0x17  <br/> |種類を結合するフィールドと、テキストフラグメントを相互に組み合わせたもの。  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>folderfielddefinitioncommon Stream 構造

folderfielddefinitioncommon stream 構造には、folderfielddefinitioncommon と folderfielddefinitioncommon の両方に共通するユーザー定義のフィールド定義のデータが含まれています。
  
このストリームの Data 要素は、次の指定された順序で互いに直後に、リトルエンディアンバイト順に格納されます。
  
- **propsetguid**: guid (16 バイト)。このプロパティには、フォルダーフィールドの対応する MAPI プロパティ名の guid が設定されます。 このフィールドの値は、PS_PUBLIC_STRINGS に等しくなければなりません。ただし、フィールドの種類が**ftnone**の場合、このフィールドの値は GUID_NULL と同じでなければなりません。 
    
   > [!NOTE]
   > 以前のバージョンとの互換性を保つために、Outlook では、この制限に該当しない**propsetguid**値の一部を処理できることがありますが、このような場合はこのトピックでは説明しません。 
  
- **fcapm**: DWORD (4 バイト) (0 個以上のフラグの組み合わせ) 次の表に、値と意味を示します。 同じ値を持つフラグは、フィールドの型、つまり fldtype の値に依存する意味を持っています。
    
    |フラグ名|値|意味|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |フィールドは編集できます。  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |フィールドは並べ替え可能です。  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |フィールドは groupable です。  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |フィールドには複数行のテキストを含めることができます。  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |ftfloat 型のこのフィールドは、パーセンテージフィールドです。  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |fttime 型のこのフィールドは、日付のみの時間フィールドです。  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |ftinteger 型のこのフィールドでは、表示形式では単位を使用できません。たとえば、"Computer-640 K..." のような形式を使用します。許可されていません。  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |このフィールドは、アイテム内で編集できます。これは、特にユーザー設定フォームの場合です。  <br/> |
   
- **dwstring**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwbitmap**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwdisplay**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **ifmt**: INT (4 バイト)。 [新しいフィールド]、[編集フィールド]、および [フィールドプロパティ] ダイアログボックスに "Format:" というコンボボックスがあるフィールドの種類については、そのコンボボックスで選択されている形式の0から始まるインデックス番号を指定します。 そのコンボボックスのないフィールド型の場合は、0である必要があります。 フィールド型の値を使用して、 **dwstring**、 **dwstring**、および**dwstring**の各フィールドの値を一意に特定するには、最初に次の注意事項を参照してください。
    
- **wszFormulaLength**: WORD (2 バイト)。 **wszFormulaLength**配列内の要素の数。
    
- **wszFormulaLength**: WCHAR の配列。 これは、標準形式でのフィールドの数式文字列の Unicode (utf-16) 表現です。 フィールドの数式の標準および UI 書式の説明については、2番目の注意事項を参照してください。 この配列の数は、 **wszFormulaLength**と同じです。 フィールド型が**ftcalc**、 **ftcalc** 、または**ftcalc**の場合を除き、式の文字列は空の文字列である必要があります。
    
> [!NOTE]
> **dwstring**、 **dwstring**、および**dwstring**の値は、 **fldtype**の値および**ifmt**値に基づいて一意に決定されますが、適切な値は正しい値になる必要があります。Outlook によるフィールド定義の処理。 この判断を実行するアルゴリズムの簡単な説明はありません。 
> 
> そのため、指定した**fldtype**値および**ifmt**値に対応する**dwstring**、 **dwstring**、および**dwstring**の値を確認するには、その種類のユーザー定義フィールドを作成し、その形式を選択してテストを実行します。適用性を想定して、[**書式**] コンボボックスで、ユーザー定義フィールドに対して Outlook によって作成された結果の**folderuserfields**ストリームを調べます。 
  
UI 形式のフィールドの数式は、ユーザー定義フィールドの [**新規フィールド**]、[**編集フィールド**]、および [**フィールドプロパティ**] ダイアログボックスの [**式**] テキストボックスで編集されます。 次に示すように、UI 形式から標準形式に数式を変換するアルゴリズムは、フィールドの種類によって異なります。 
- 種類が**ftcalc**および**ftcalc**のフィールドについては、組み込みフィールドの標準形式 (対応する MAPI プロパティは、kind MNID\_STRING のプロパティと名前が付けられていません) は`[<field_name>]` 、フィールド名のフラグメントを置換することによって取得されます。フラグメント`[_<field_dispid_decimal>]`を使用します。 

  たとえば、 **ftcalc**という名前の`[Business Phone] & [My custom field]`**式**のフィールドに対する式の UI 書式が、Office UI 言語が英語`My custom field`の場合、ユーザー定義フィールドの名前である場合、そのような数式の標準形式は次のようになります。`[_14856] & [My custom field]`.

- 型**ftconcat**のフィールドについては、次の手順を実行して標準形式を取得します。

  1. 先頭および末尾の空白文字を切り捨てます。 
  2. 数式を解析して、次の2種類の一連のフラグメントにします。 
     - 角かっこで囲まれたフィールド名 (つまり`[<field_name>]`、)。 
     - 角かっこが含まれていない部分文字列。   
      2番目の種類の2つのフラグメントがシーケンス内で隣接していないことを保証します。 この方法で数式を解析できない場合は、無効であると見なされます。 
  3. **ftcalc**フィールドおよび**ftcalc**フィールドに対して、最初の種類のフラグメントに対して同じ置換を実行します。 
  4. 2番目の種類の各フラグメントに対して、二重引用符 ("") 文字がある場合は、二重引用符を2つ続けてエスケープし、二重引用符で囲みます。 
  5. 隣接する一連のフラグメント`&`間に、アンパサンド文字列 () を挿入します。
 
  たとえば、「 **ftconcat** `text1 [Business Phone] "text2" [My custom field]` `My custom field` 」という型のフィールドの数式の ui 形式を使用している場合、このような数式の標準形式は、Office UI 言語の英語 (米国) を使用して`""text1" & [_14856] & """text2""" & [My custom field]"`います。 
  
## <a name="see-also"></a>関連項目

- [folderuserfields ストリームのサンプル](folderuserfields-stream-sample.md)
- [新しいユーザー定義フィールドの定義を追加する](how-to-add-a-definition-for-a-new-user-defined-field.md)

