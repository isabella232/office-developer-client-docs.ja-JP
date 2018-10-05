---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Outlook 予定表で予定を再配置で使用する IOlkApptRebaser オブジェクトを初期化します。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397542"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Outlook 予定表で予定を再配置で使用する[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |tzmovelib.h  <br/> |
|実装元:  <br/> |tzmovelib.dll  <br/> |
|呼び出し元:  <br/> |MAPI クライアント アプリケーション  <br/> |
|ポインターの型。  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|DLL エントリ ポイント:  <br/> |**HrCreateApptRebaser@44** <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a>�p�����[�^�[

_ulFlags_
  
> [in]必要があります。 再配置の実行方法を制御するためのフラグのビットマスクです。 次のフラグが設定でき、tzmovelib.h で定義されています。
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** -ユーザーは、会議の開催者の予定表アイテムが再配置されます。 既定では、こうすると、再配置されているすべての会議のすべての出席者に会議の更新を送信する Outlook に注意してください。 **REBASE_FLAG_FORCE_NO_EX_UPDATES**または**REBASE_FLAG_FORCE_NO_UPDATES**のいずれかが会議の更新の処理方法を変更するのには、このフラグを組み合わせることができます。 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** -タイム ゾーンに設定されていない予定表アイテムを更新します。 このフラグを指定する場合にアイテムが作成されるタイム ゾーンとタイム ゾーン データがないすべてのアイテムの*pTZMissing*値が使用されます。 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** -唯一の定期的な予定アイテムを更新します。 
    
   - **REBASE_FLAG_NO_UI** -ログオン ダイアログ ボックスのメッセージ ストアを開くときに一般に表示されるなど、ユーザー インターフェイス (UI) を表示しません。 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** -過去の予定表アイテムが再配置されません。 
    
   - **REBASE_FLAG_FORCE_REBASE** -上の決定を再配置するための開催者を確認しないが、ユーザーは、出席者の予定表アイテムを再配置します。 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** -ユーザーが開催者であり、受信者が、Exchange Server に接続されていない場合にのみ更新を送信します。 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** : 更新プログラムを送信することはありません。 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** -修正プログラムを適用する前に作成された単独の予定アイテムのみを再配置します。 
    
   - **REBASE_FLAG_REPORTING_MODE** -再実際には、単なるレポートの予定アイテムを再配置されます。 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** -リソースに会議の更新を送信します。 
    
_pSession_
  
> [in]必要があります。 MAPI セッションのインターフェイスへのポインター。
    
_pCalendarMsgStore_
  
> [in]必要があります。 再配置する予定のアイテムを含むメッセージ ストアへのポインター。
    
_pCalendarFolder_
  
> [in]必要があります。 再配置する予定のアイテムが含まれている予定表フォルダーへのポインター。
    
_pwszUpdatePrefix_
  
> [in]省略可能です。 会議出席依頼の前に付加するプレフィックスを含む文字列へのポインター。 NULL である可能性があります。
    
_pftInstallDateUTC_
  
> [in]省略可能です。 タイム ゾーン更新プログラムでは、日付をインストールします。 **REBASE_FLAG_ONLY_CREATED_PRE_PATCH**フラグが設定されている場合にのみ使用されます。 
    
_IExpansionDepth_
  
> [in]省略可能です。 配布を展開する Exchange Server に接続されている受信者を除外する一覧に表示するときの拡張の深さです。 **REBASE_FLAG_FORCE_NO_EX_UPDATES**フラグが設定されている場合にのみ使用します。 
    
_pTZTo_
  
> [in]必要があります。 再配置するタイム ゾーンを記述する**TZDEFINITION**構造体へのポインター。 **TZDEFINITION**は、tzmovelib で定義されます。 
    
pTZMissing
  
> [in]必要があります。 アイテムにタイム ゾーン情報がスタンプされていないかどうかを前提とするタイム ゾーンを記述する**TZDEFINITION**構造体へのポインター。 できませんが NULL の場合、 **REBASE_FLAG_UPDATE_UNMARKED**フラグが設定されている場合に使用します。 
    
_ppError_
  
> [out]エラーのバージョン、コンポーネント、およびコンテキストの情報を保持する**MAPIERROR**構造体へのポインターへのポインター。 拡張エラー情報が必要ない場合、NULL にすることができます。 [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)を解放します。 
    
_ppApptRebase_
  
> [out]返される**IOlkApptRebaser**インターフェイスへのポインターへのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用して、tzmovelib.dll では、この関数のアドレスを検索するのには、プロシージャ名として**HrCreateApptRebaser@44**を指定します。 すべてのフラグは、相互の組み合わせで有効です。 
  
さまざまなオプションの詳細についてを参照してください「Outlook タイム ゾーン データ更新ツールのコマンド ライン オプションの用語集」で[KB 931667: Microsoft Office Outlook 用タイム ゾーン データ更新ツールを使用してアドレスのタイム ゾーンの変更方法](https://support.microsoft.com/kb/931667/en-us)。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

