---
title: EditRecord データ ブロック (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: EditRecord データ ブロックを使用して、既存のレコード内の値を変更できます。
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798565"
---
# <a name="editrecord-data-block-access-custom-web-app"></a>EditRecord データ ブロック (カスタム web アプリケーションのアクセス)

**EditRecord** データ ブロックを使用して、既存のレコード内の値を変更できます。 
  
> [!IMPORTANT]
> マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。 
  
> [!NOTE]
> [!メモ] **EditRecord** データ ブロックは、データ マクロでのみ使用できます。 
  
## <a name="setting"></a>設定

**EditRecord** データ ブロックの引数は次のとおりです。 
  
|**引数**|**説明**|
|:-----|:-----|
|**エイリアス** <br/> |編集するレコードを識別する文字列です。 *別名*引数を指定しない場合、現在のレコードを編集します。  <br/> |
   
## <a name="remarks"></a>注釈

**EditRecord** ステートメントの後に、レコードの変更を確定する前に実行するコマンドのブロックを挿入できます。 **EditRecord** データ ブロックで使用できるアクションは次のとおりです。 
  
||
|:-----|
|["CancelRecordChange/レコードの変更の取り消し" マクロ アクション](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[Comment マクロ ステートメント](comment-macro-block-access-custom-web-app.md) <br/> |
|[Group マクロ ステートメント](group-macro-block-access-custom-web-app.md) <br/> |
|[もし。。。そうしたら。。。マクロ ステートメントはその他](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|["SetField/フィールドの設定" マクロ アクション](setfield-macro-action-access-custom-web-app.md) <br/> |
|["SetLocalVar/ローカル変数の設定" マクロ アクション](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
" **SetField** /フィールドの設定" アクションを使用して、編集するレコードの新しいフィールド値を指定します。 
  
条件に基づいて操作を実行する場合は **If...Then...Else** ステートメントを使用できます。 
  
レコードの編集を取り消すには、" **CancelRecordChange** /レコードの変更の取り消し" アクションを使用します。これにより、変更は確定されずに、 **EditRecord** データ ブロックが終了します。 
  
**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで作成した一番新しいレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードの AssignedTo フィールドを参照します。 
  
`[LastCreateRecordIdentity].[AssignedTo]`


