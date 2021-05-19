---
title: フォルダー フィールド ストリーム構造
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336891"
---
# <a name="folder-fields-stream-structures"></a>フォルダー フィールド ストリーム構造

**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの [PidTagUserFields](pidtaguserfields-canonical-property.md) プロパティには、フォルダーのユーザー定義フィールド定義を含むバイナリ ストリーム FolderUserFields が含まれます。 このトピックでは、フォルダーのユーザー定義フィールド定義のストリーム構造について説明します。 

FolderUserFields ストリーム構造は、FolderUserFieldsA 構造体または FolderUserFieldsA 構造体の後に FolderUserFieldsW 構造体で構成されます。
  
このストリーム内のデータ要素は、次の指定された順序で、お互いに直後に格納されます。
  
- **FolderUserFieldsAnsi**: FolderUserFieldsA ストリーム構造。
    
- **FolderUserFieldsUnicode** (省略可能): FolderUserFieldsW ストリーム構造。
    
FolderUserFieldsUnicode の存在は、FolderUserFieldsAnsi の長さよりも大きい FolderUserFields の合計長によって検出されます。
  
> [!IMPORTANT]
> FolderUserFieldsAnsi は、古いバージョンの Unicode 以外の MAPI クライアントとの互換性のために使用されるため、FolderUserFieldsUnicode が存在する場合、FolderUserFieldsAnsi の内容は無視されます。 ANSI 変換でデータが失われる可能性を回避するには、FolderUserFields ストリームを作成するときに必ず FolderUserFieldsW パーツを含める必要があります。 
  
## <a name="folderuserfieldsa-stream-structure"></a>FolderUserFieldsA ストリーム構造

FolderUserFieldsA ストリーム構造は、FolderUserFields 構造体の FolderUserFieldsW 部分によってオーバーライドされない限り、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む FolderFieldDefinitionA ストリーム構造の配列です。
  
このストリームのデータ要素は、次の指定された順序で互いに直後に続く、リトル エンディアン バイト順に格納されます。
  
- **FieldDefinitionCount**: DWORD (4 バイト)、このストリーム内のフィールド定義の数。 これは **、FieldDefinitions 配列内の要素の数** です。
    
- **FieldDefinitions**: FolderFieldDefinitionA ストリーム構造の配列。 この配列の数は **、FieldDefinitionCount データ要素と** 等しくなります。
    
この FolderUserFieldsA が FolderUserFields 構造体の FolderUserFieldsW 部分によってオーバーライドされない限り **、FieldDefinitions** 配列は、最後の FolderFieldDefinitionA 要素の Common.FieldType フィールドを ftNull に等しくすることで"null-terminated" である必要があります。
  
## <a name="folderuserfieldsw-stream-structure"></a>FolderUserFieldsW ストリーム構造

FolderUserFieldsW ストリーム構造は、Outlook フォルダー内のすべてのユーザー定義フィールドの定義を含む FolderFieldDefinitionW ストリーム構造の配列です。
  
このストリームのデータ要素は、次の指定された順序で互いに直後に続く、リトル エンディアン バイト順に格納されます。
  
- **FieldDefinitionCount**: DWORD (4 バイト)、このストリーム内のフィールド定義の数。 これは **、FieldDefinitions 配列内の要素の数** です。
    
- **FieldDefinitions**: FolderFieldDefinitionW ストリーム構造の配列。 この配列の数は **、FieldDefinitionCount データ要素と** 等しくなります。
    
**FieldDefinitions** 配列は、最後の FolderFieldDefinitionW 要素の Common.FieldType フィールドが ftNull に等しくなります。
  
## <a name="folderfielddefinitiona-stream-structure"></a>FolderFieldDefinitionA ストリーム構造

FolderFieldDefinitionA ストリーム構造には、ANSI に格納されているフィールド名を持つユーザー定義フィールドの定義が含まれます。
  
このストリームのデータ要素は、次の指定された順序で互いに直後に続く、リトル エンディアン バイト順に格納されます。
  
- **FieldType**: FldType (4 バイト)、このフィールドの種類。
    
- **FieldNameLength**: WORD (2 バイト **)、FieldName** 配列内の要素の数。
    
- **FieldName**: CHAR の配列。 これは、フィールド名CP_ACPコード ページ表現の ANSI です。 この配列の数は **FieldNameLength と等しくなります**。 フィールド名は [、UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) メソッドで指定されている Name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > 従来の互換性の理由から、Outlook ではこれらの制限を満たしていない **FieldName** 値を処理できる場合があります。ただし、このようなケースについては、このトピックでは説明しない場合があります。 
  
- **共通**: FolderFieldDefinitionCommon ストリーム構造。
    
## <a name="folderfielddefinitionw-stream-structure"></a>FolderFieldDefinitionW ストリーム構造

FolderFieldDefinitionW ストリーム構造には、Unicode に格納されているフィールド名を持つユーザー定義フィールドの定義が含まれます。
  
このストリームのデータ要素は、次の指定された順序で互いに直後に続く、リトル エンディアン バイト順に格納されます。
  
- **FieldType**: FldType (4 バイト)、このフィールドの種類。
    
- **FieldNameLength**: WORD (2 バイト **)、FieldName** 配列内の要素の数。
    
- **FieldName**: WCHAR の配列。 これは、フィールド名の Unicode (UTF-16) 表記です。 この配列の数は **FieldNameLength と等しくなります**。 フィールド名は [、UserProperties.Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) メソッドで指定されている Name パラメーターの制限を満たす必要があります。 
    
   > [!NOTE]
   > 従来の互換性の理由から、Outlook ではこれらの制限を満たしていない **FieldName** 値を処理できる場合がありますが、このようなケースについては、このトピックでは説明しない場合があります。 
  
- **共通**: FolderFieldDefinitionCommon ストリーム構造。
    
## <a name="fldtype-enumeration"></a>FldType 列挙

**FldType** 列挙値を次の表に示します。 
  
|名前|値|意味|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |このフィールド型は、フィールド定義の配列を null で終了するために使用されます。  <br/> |
|ftString  <br/> |0x1  <br/> |テキスト  <br/> |
|ftInteger  <br/> |0x3  <br/> |整数  <br/> |
|ftTime  <br/> |0x5  <br/> |日付/時刻  <br/> |
|ftBoolean  <br/> |0x6  <br/> |はい/いいえ  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0xB  <br/> |キーワード  <br/> |
|ftFloat  <br/> |0xC  <br/> |数値またはパーセント  <br/> |
|ftCurrency  <br/> |0xE  <br/> |通貨  <br/> |
|ftCalc  <br/> |0x12  <br/> |式  <br/> |
|ftSwitch  <br/> |0x13  <br/> |最初の空でないフィールドのみを表示する型の組み合わせ - 後続のフィールドを無視します。  <br/> |
|ftConcat  <br/> |0x17  <br/> |結合フィールドの型とテキスト フラグメントの組み合わせ。  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>FolderFieldDefinitionCommon ストリーム構造

FolderFieldDefinitionCommon ストリーム構造には、FolderFieldDefinitionA と FolderFieldDefinitionW の両方に共通するユーザー定義フィールド定義のデータが含まれます。
  
このストリームのデータ要素は、次の指定された順序で互いに直後に続く、リトル エンディアン バイト順に格納されます。
  
- **PropSetGuid**: GUID (16 バイト)、フォルダー フィールドの対応する MAPI プロパティ名のプロパティ セット GUID。 このフィールドの値は、フィールドの種類が **ftNone** の場合、このフィールドの値が GUID_NULL と等しい場合を指定しない限り、PS_PUBLIC_STRINGS と等しくする必要があります。 
    
   > [!NOTE]
   > 従来の互換性の理由から、Outlook は、この制限を満たしていない一部の **PropSetGuid** 値を処理できる場合があります。ただし、このようなケースについては、このトピックでは説明されません。 
  
- **fcapm**: DWORD (4 バイト)、ゼロ以上の組み合わせで、値と意味を次の表に示します。 同じ値を持つフラグは、フィールドの種類 、つまり FldType 値に依存する意味を持ちます。
    
    |フラグ名|値|意味|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |フィールドは編集可能です。  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |フィールドは並べ替え可能です。  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |フィールドはグループ化可能です。  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |フィールドには複数行のテキストを保持できます。  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |ftFloat 型のこのフィールドはパーセンテージ フィールドです。  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |ftTime 型のこのフィールドは、日付専用の時刻フィールドです。  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |ftInteger 型のこのフィールドでは、表示形式で単位を使用できます。たとえば、"Computer - 640 K.." などの形式。は許可されません。  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |フィールドはアイテムで編集できます。これは特にカスタム フォーム用です。  <br/> |
   
- **dwString**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwBitmap**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **dwDisplay**: DWORD (4 バイト)。 最初の次の注を参照してください。
    
- **iFmt**: INT (4 バイト)。 "New Field"、"Edit Field"、"Field Properties" ダイアログの "Format:" コンボ ボックスを持つフィールド型の場合、そのコンボ ボックスで選択された形式の 0 からベースのインデックス。 そのコンボ ボックスのないフィールドの種類の場合、これは 0 である必要があります。 フィールドの値とフィールドの種類によって **、dwString フィールド、dwBitmap** フィールド、**および****dwDisplay** フィールドの値が一意に決定されます。最初の次の注を参照してください。
    
- **wszFormulaLength**: WORD (2 バイト **)、wszFormulaLength** 配列内の要素の数。
    
- **wszFormulaLength**: WCHAR の配列。 これは、フィールドの数式文字列を標準形式で表す Unicode (UTF-16) 表記です。 フィールドの数式の標準形式と UI 形式の説明については、次の 2 番目の注を参照してください。 この配列の数は **wszFormulaLength と等しくなります**。 フィールドの種類が **ftCalc、ftSwitch、****または ftConcat** の場合を指定しない限り、数式文字列は空の **文字列である必要があります**。
    
> [!NOTE]
> **dwString、dwBitmap、****および dwDisplay** の値は **、FldType** 値と **iFmt** 値に基づいて一意に決定されます。冗長ですが、Outlook によるフィールド定義の正しい処理には、正しい値が必要です。  この決定を実行するアルゴリズムの簡単な説明はありません。 
> 
> したがって、指定された **FldType** 値と **iFmt** 値に対応する **dwString** 値 **、dwBitmap** 値、および **dwDisplay** 値を確認するには、その型のユーザー定義フィールドを作成してテストを実行し、その形式を [書式] コンボ ボックスで選択し、適用性を前提として、Outlook が作成する **FolderUserFields** ストリームをそのユーザー定義フィールドに対して検査します。 
  
UI 形式のフィールドの数式は、ユーザー定義フィールドの[新しいフィールド]、[フィールドの編集]、および [フィールド のプロパティ] ダイアログ ボックスの [数式] テキスト ボックスで編集されます。   数式を UI 形式から標準形式に変換するアルゴリズムは、次に示すフィールドの種類によって異なります。 
- **ftCalc** 型と **ftSwitch** 型のフィールドでは、組み込みフィールドの標準形式であり、対応する MAPI プロパティは、MNID STRING の種類の名前付きプロパティではなく、フィールド名フラグメントをフラグメントに置き換えた結果を取得します。 \_ `[<field_name>]` `[_<field_dispid_decimal>]` 

  たとえば、数式型のフィールドの UI 形式が **ftCalc** で、Office UI 言語が米国英語である場合、ユーザー定義フィールドの名前は 、このような数式の標準形式になります。 `[Business Phone] & [My custom field]` `My custom field` `[_14856] & [My custom field]`

- **ftConcat** 型のフィールドの場合、標準の形式は以下を実行して取得されます。

  1. 先頭と末尾の空白を切り捨てる。 
  2. 次の 2 種類のフラグメントのシーケンスに数式を解析します。 
     - 角かっこで囲まれたフィールド名、つまり、 `[<field_name>]` を指定します。 
     - 角かっこを含む部分文字列。   
      2 番目の種類の 2 つのフラグメントがシーケンス内で隣接しないなことを確認します。 この方法で数式を解析できない場合は、無効と見なされます。 
  3. ftCalc フィールドおよび **ftSwitch** フィールドと同じ種類のフラグメントに対して同じ置換 **を実行** します。 
  4. 2 番目の種類のフラグメントごとに、すべての二重引用符 (""") 文字がある場合は、2 つの連続する二重引用符文字をエスケープし、二重引用符で囲む必要があります。 
  5. 隣接するフラグメントの各ペアの間にアンパサンド文字列 ( `&` ) を挿入します。
 
  たとえば、Office UI 言語の米国英語を使用して **、ftConcat** 型のフィールドの数式の UI 形式が 、ユーザー定義フィールドの名前である場合、そのような数式の標準書式になります。 `text1 [Business Phone] "text2" [My custom field]` `My custom field` `""text1" & [_14856] & """text2""" & [My custom field]"` 
  
## <a name="see-also"></a>関連項目

- [FolderUserFields ストリームのサンプル](folderuserfields-stream-sample.md)
- [新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)

