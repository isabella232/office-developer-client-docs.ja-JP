---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Outlook の予定表で予定を再配置するときに使用する IOlkApptRebaser オブジェクトを初期化します。
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317613"
---
# <a name="hrcreateapptrebaser"></a>HrCreateApptRebaser

Outlook の予定表で予定を再配置するときに使用する[IOlkApptRebaser](iolkapptrebaser.md)オブジェクトを初期化します。 
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |、tzmovelib.h  <br/> |
|実装元:  <br/> |、tzmovelib.h  <br/> |
|呼び出し元:  <br/> |MAPI クライアントアプリケーション  <br/> |
|ポインターの種類:  <br/> |**LPHRCREATEAPPTREBASER** <br/> |
|DLL エントリポイント:  <br/> |**hrcreateapptrebaser @ 44** <br/> |
   
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

## <a name="parameters"></a>パラメーター

_ulFlags_
  
> [in]必要があります。 リベースの実行方法を制御するために使用されるフラグのビットマスク。 、tzmovelib.h では、次のフラグを設定および定義できます。
    
   - **REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —ユーザーが会議の開催者になっている予定アイテムが再配置されます。 既定では、この設定により、再配置されているすべての会議の出席者全員に会議の更新が送信されることに注意してください。 このフラグを**REBASE_FLAG_FORCE_NO_EX_UPDATES**または**REBASE_FLAG_FORCE_NO_UPDATES**と組み合わせて、会議の更新の処理方法を変更することができます。 
    
   - **REBASE_FLAG_UPDATE_UNMARKED** —タイムゾーンが設定されていない予定アイテムを更新します。 このフラグが指定されている場合は、タイムゾーンデータを持たないすべてのアイテムに対してアイテムが作成されるタイムゾーンとして、 *ptzmissing*の値が使用されます。 
    
   - **REBASE_FLAG_UPDATE_ONLYRECURRING** -定期的な予定アイテムのみを更新します。 
    
   - **REBASE_FLAG_NO_UI** —メッセージストアを開くときに通常表示されるログオンダイアログボックスなど、ユーザーインターフェイス (UI) を表示しません。 
    
   - **REBASE_FLAG_UPDATE_MINIMIZEAPPTS** -過去に発生した予定アイテムを再配置しません。 
    
   - **REBASE_FLAG_FORCE_REBASE** —開催者による再配置の決定をチェックせず、ユーザーが出席者になっている予定アイテムを再配置します。 
    
   - **REBASE_FLAG_FORCE_NO_EX_UPDATES** —ユーザーが開催者であり、受信者が Exchange サーバーに接続されていない場合にのみ、更新を送信します。 
    
   - **REBASE_FLAG_FORCE_NO_UPDATES** -更新を送信しません。 
    
   - **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** -パッチを適用する前に作成された単一インスタンスの予定アイテムのみをリベースします。 
    
   - **REBASE_FLAG_REPORTING_MODE** -再配置される予定アイテムを報告するだけで、実際には再配置しないようにします。 
    
   - **REBASE_FLAG_SEND_RESOURCE_UPDATES** —リソースに会議の更新を送信します。 
    
_psession_
  
> [in]必要があります。 MAPI セッションインターフェイスへのポインター。
    
_pcalendarmsgstore_
  
> [in]必要があります。 再配置する予定アイテムを含むメッセージストアへのポインター。
    
_pcalendarfolder_
  
> [in]必要があります。 再配置する予定アイテムを含む予定表フォルダーへのポインター。
    
_pwszUpdatePrefix_
  
> [in]省略可能です。 会議出席依頼の先頭に付加するプレフィックスを含む文字列へのポインター。 NULL の場合があります。
    
_pftinstalldateutc_
  
> [in]省略可能です。 タイムゾーンパッチのインストールの日付。 **REBASE_FLAG_ONLY_CREATED_PRE_PATCH**フラグが設定されている場合にのみ使用します。 
    
_i の色_
  
> [in]省略可能です。 Exchange Server に接続されている受信者を除外するために配布リストを展開するときの拡張の深さ。 **REBASE_FLAG_FORCE_NO_EX_UPDATES**フラグが設定されている場合にのみ使用されます。 
    
_ptzto_
  
> [in]必要があります。 再配置するタイムゾーンを記述する**TZDEFINITION**構造体へのポインター。 **TZDEFINITION**は、、tzmovelib.h で定義されています。 
    
ptzmissing
  
> [in]必要があります。 タイムゾーン情報がアイテムにスタンプされていない場合に想定されるタイムゾーンを説明する**TZDEFINITION**構造体へのポインター。 NULL にすることはできませんが、 **REBASE_FLAG_UPDATE_UNMARKED**フラグが設定されている場合にのみ使用されます。 
    
_pperror_
  
> 読み上げエラーのバージョン、コンポーネント、およびコンテキスト情報を含む**MAPIERROR**構造体へのポインターへのポインター。 拡張エラー情報を必要としない場合は、NULL を指定できます。 [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx)を使用して無料で使用できます。 
    
_ppapptrebase_
  
> 読み上げ返された**IOlkApptRebaser**インターフェイスへのポインターへのポインター。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解説

[GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx)を使用して、tzmovelib.h でこの関数のアドレスを検索する場合は、プロシージャ名として**hrcreateapptrebaser @ 44**を指定します。 すべてのフラグが互いに組み合わせて有効なわけではありません。 
  
さまざまなオプションの詳細については、「 [KB 931667: time zone data update tool for Microsoft Office Outlook を使用してタイムゾーンの変更に対処する方法](https://support.microsoft.com/kb/931667/en-us)」の「Outlook タイムゾーンデータ更新ツールのコマンドラインオプションの用語集」を参照してください。
  
## <a name="see-also"></a>関連項目

- [夏時間のプログラムを使用して予定表を再配置する方法](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

