---
title: EditRecord Data Block (Access custom Web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: EditRecord データ ブロックを使用して、既存のレコード内の値を変更できます。
ms.openlocfilehash: 8e179eb08d5624adb58a72576ac816126e0a8edc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621494"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>EditRecord Data Block (Access custom Web app)

You can use the **EditRecord** data block to change the values contained in an existing record. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> EditRecord データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

**EditRecord** データ ブロックの引数は次のとおりです。 
  
|**Arg1 と Arg2 の値**|**説明**|
|:-----|:-----|
|**Alias** <br/> |編集するレコードを識別する文字列。 引数  *Alias を指定*  しない場合は、現在のレコードが編集されます。  <br/> |
   
## <a name="remarks"></a>注釈

**EditRecord** ステートメントの後に、レコードの変更を確定する前に実行するコマンドのブロックを挿入できます。**EditRecord** データ ブロックで使用できるアクションは次のとおりです。 
  
||
|:-----|
|["CancelRecordChange/レコードの変更の取り消し" マクロ アクション](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment マクロ ステートメント](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group マクロ ステートメント](group-macro-block-access-custom-web-app.md) <br/> |
|[If...Then...Else マクロ ステートメント](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|["SetField/フィールドの設定" マクロ アクション](setfield-macro-action-access-custom-web-app.md) <br/> |
|["SetLocalVar/ローカル変数の設定" マクロ アクション](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。 
  
条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。 
  
レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。 
  
**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで作成した一番新しいレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。 
  
`[LastCreateRecordIdentity].[AssignedTo]`


