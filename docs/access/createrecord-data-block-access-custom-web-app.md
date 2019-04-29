---
title: CreateRecord データブロック (Access カスタム web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: CreateRecord データ ブロックを使用して、指定したテーブルに新しいレコードを作成できます。
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421376"
---
# <a name="createrecord-data-block-access-custom-web-app"></a>CreateRecord データブロック (Access カスタム web アプリ)

You can use the **CreateRecord** data block to create a new record in the specified table. 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> **CreateRecord** データ ブロックはデータ マクロでのみ使用できます。 
  
## <a name="setting"></a>Setting

**CreateRecord** データ ブロックの引数は次のとおりです。 
  
**CreateRecord** データ ブロックの引数は次のとおりです。 
  
|**引数名**|**必須**|**説明**|
|:-----|:-----|:-----|
|**Create a Record In**/レコードの作成先 <br/> |はい  <br/> |新しいレコードを作成するテーブルの名前。  <br/> |
|**Alias** <br/> |いいえ  <br/> |レコードを識別する文字列。レコードの別名を使用できます。  <br/> |
   
## <a name="remarks"></a>注釈

**CreateRecord** で作成したレコードは自動的にカレント レコードになります。 
  
**CreateRecord** ステートメントの後に、新しいレコードの作成を確定する前に実行するコマンドのブロックを挿入できます。 **CreateRecord** データ ブロックで使用できるアクションは次のとおりです。 
  
||
|:-----|
|["CancelRecordChange/レコードの変更の取り消し" マクロ アクション](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment マクロ ステートメント](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group マクロ ステートメント](group-macro-block-access-custom-web-app.md) <br/> |
|[If...Then...Else マクロ ステートメント](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|["SetField/フィールドの設定" マクロ アクション](setfield-macro-action-access-custom-web-app.md) <br/> |
|["SetLocalVar/ローカル変数の設定" マクロ アクション](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
" **CreateRecord** /レコードの作成" アクションでレコードを作成した後、" **SetField** /フィールドの設定" アクションを使用して、新しいレコードのフィールド値を指定します。 
  
条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。 
  
レコードの作成を取り消すには " **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **CreateRecord** データ ブロックが終了します。 
  
新しいレコードの作成を確定すると、 **LastCreateRecordIdentity** ローカル変数を使用してレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。 
  
`[LastCreateRecordIdentity].[AssignedTo]`


