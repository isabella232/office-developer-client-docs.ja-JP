---
title: POP3 アカウントのメッセージ ダウンロード履歴の検索
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: このトピックでは、メール クライアントが PidTagAttachDataBinary プロパティにアクセスして POP3 アカウントのメッセージダウンロード履歴を取得する方法について説明します。
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321876"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の検索

このトピックでは、メール クライアントが [PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx) プロパティにアクセスして POP3 アカウントのメッセージダウンロード履歴を取得する方法について説明します。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>メッセージのダウンロード履歴を取得する理由

Outlook の post Office プロトコル (POP) プロバイダーを使用すると、ユーザーはローカル デバイスで新しい電子メール メッセージを取得およびダウンロードし、その後、メール サーバー上でこれらの電子メール メッセージを残したり削除したりできます。 メール クライアントは、ダウンロードする新しいメッセージをチェックするときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。 メール クライアントは、まず UIDL (Unique ID Listing) コマンドを使用してこれを行い、受信トレイに配信された各メッセージのマップを一意の識別子 (UID) に取得します。 クライアントは、そのクライアントの受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。 メッセージ UID マップとダウンロード履歴を使用して、クライアントは履歴に存在しないメッセージを新しいメッセージとして識別し、したがってダウンロードする必要があります。
  
受信トレイのメッセージダウンロード履歴を取得するには、次の方法を実行します。
  
- このトピックの手順に従って、特定の形式に従うバイナリ ラージ オブジェクト (BLOB) の履歴を含む **PidTagAttachDataBinary** プロパティを検索します。 
    
- POP3 [アカウントの](parsing-the-message-download-history-for-a-pop3-account.md)メッセージダウンロード履歴の解析に進み、この BLOB を解析して、その受信トレイに対してダウンロードまたは削除されたメッセージを識別する方法について説明します。
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>メッセージのダウンロード履歴を見つけ出す上で知る重要な概念

受信トレイのメッセージダウンロード履歴は、バイナリ MAPI プロパティ **PidTagAttachDataBinary** に、受信トレイ内の非表示メッセージの添付ファイルに格納されます。 表 1 に、メッセージのダウンロード履歴を見つける方法を理解するのに役立つ概念のリソースを示します。
  
**表 1. 中心概念**

|**記事のタイトル**|**説明**|
|:-----|:-----|
|[MAPI 隠しフォルダー](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI を使用すると、メール クライアントは非表示のフォルダーと非表示のメッセージに情報を格納できます。 非表示のフォルダーは、MAPI フォルダーの関連付けられた部分に含まれています。通常、ユーザーが操作する情報ではなく、表示されない情報が含まれます。 クライアントは、非表示のメッセージを非表示フォルダーに格納する形式とコンテンツを決定します。  <br/> |
|[MAPI メッセージ](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI は、クライアントのユーザーに表示される標準 IPM サブツリー、またはサブツリーの外部に表示され、ユーザーには表示されないフォルダーにメッセージを格納します。 メッセージには、ファイル、別のメッセージ、または OLE オブジェクトの形式で、添付ファイルに追加のデータを格納できます。 メッセージのダウンロード履歴の場合、履歴は、別の非表示メッセージに添付されているメッセージのプロパティに格納されます。  <br/> |
|[メッセージ のプロパティの概要](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |クライアントがメッセージに情報を格納すると、実際にはメッセージのプロパティに情報が格納されます。 MAPI では、多くのプロパティがサポートされています。一部は常に存在し、クライアントによって設定できます。他のプロパティはオプションです。また、クライアントはそれらを使用可能にしたり、有効な値に設定したりすることはできません。 メッセージのダウンロード履歴は、非表示のメッセージへの添付ファイル **の PidTagAttachDataBinary** プロパティに格納されます。  <br/> |
|[MAPI プロファイル](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |セッションのログオン時に、メール クライアントは、使用するプロバイダーとサービスを説明するプロファイルを選択します。 プロファイルは、プロパティを含むセクションに分かれています。 特に [、PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) **(** PR_SEARCH_KEY ) および [PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) ( PR_PROFILE_NAME ) プロパティ **は** 常に存在します。 プロファイルの検索キーは、すべてのプロファイル間で一意であり、MAPIGUID で定義されている MUID_PROFILE_INSTANCE によって識別 **される** プロファイル セクションに格納されます。H)。 [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx)を使用してセクションを開き[、IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)を使用してプロパティ値を取得します。  <br/> |
|[コンテンツ テーブル](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |メッセージ ストア プロバイダーは、フォルダーのコンテンツ テーブルを実装します。 フォルダーの関連付けられた部分の非表示メッセージの場合、メッセージ ストア プロバイダーは関連付けられたコンテンツ テーブルをサポートし、クライアントは [IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx) メソッドを使用して、関連付けられたコンテンツ テーブルへのポインターを返します。  <br/> |
|[制限について](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [制限の種類](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [制限の作成](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [制限コードの例](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |MAPI では、クライアントは制限を使用してコンテンツ テーブルをフィルター処理し、特定のプロパティが特定の値に設定されているメッセージを表す行を検索できます。 制限は、より特殊な制限構造の共用体を含む [SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx) データ構造を使用して定義されます。 [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx)メソッドは、制限を適用し、制限条件に一致するテーブルの最初の行を取得します。  <br/> |
|[概要 - インデックス作成用のストアの登録](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |[PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) **(** PR_MDB_PROVIDER ) プロパティを使用して、ストア プロバイダーの種類を確認します。 たとえば、ストアが Exchange ストアであるかどうかを確認するには **、PidTagStoreProvider** プロパティは、パブリック ヘッダー ファイル edkmdb.h で定義されている **定数 pbExchangeProviderPrimaryUserGuid** で表される値を返す必要があります。  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>適切な非表示のメッセージと添付ファイルを見つける

受信トレイのメッセージダウンロード履歴が、非表示メッセージへの添付ファイルの **PidTagAttachDataBinary** プロパティに含まれるので、適切な非表示メッセージの適切な添付ファイルを見つける手順には、次の手順が含まれます。 
  
1. [適切な非表示メッセージを見つける](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [非表示のメッセージの適切な添付ファイルを検索する](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [メッセージ添付ファイルの PidTagAttachDataBinary プロパティにアクセスする](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>適切な非表示メッセージを見つける

1. プロファイルから [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) **(** PR_SEARCH_KEY ) プロパティを取得します。このプロパティは、プロファイルで指定されたプロファイル セクション **MUID_PROFILE_INSTANCE。**
    
2. **IMAPIContainer::GetContentsTable** を呼び出して受信トレイ フォルダーの関連コンテンツを開きます。
    
3. [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (PR_CONVERSATION_KEY)、PidTagSearchKey **(PR_SEARCH_KEY)、** および [PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) ( PR_MESSAGE_CLASS ) プロパティに基づいて制限を作成し、受信トレイの関連コンテンツ内のすべての非表示メッセージを含むテーブルを取得します。  POP3 UIDL 履歴の検索から抽出された制限の例 [を次に示します](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)。
    
   ```cpp
      SRestriction rgRes[3]; 
      SPropValue rgProps[3]; 
      rgRes[0].rt = RES_AND; 
      rgRes[0].res.resAnd.cRes = 2; 
      rgRes[0].res.resAnd.lpRes = &amp;rgRes[1]; 
      rgRes[1].rt = RES_PROPERTY; 
      rgRes[1].res.resProperty.relop = RELOP_EQ; 
      rgRes[1].res.resProperty.ulPropTag = PR_CONVERSATION_KEY; 
      rgRes[1].res.resProperty.lpProp = &amp;rgProps[0]; 
      rgRes[2].rt = RES_PROPERTY; 
      rgRes[2].res.resProperty.relop = RELOP_EQ; 
      rgRes[2].res.resProperty.ulPropTag = PR_MESSAGE_CLASS; 
      rgRes[2].res.resProperty.lpProp = &amp;rgProps[1]; 
      rgProps[0].ulPropTag = PR_CONVERSATION_KEY; 
      rgProps[0].Value.bin = pVals[iSearchKey].Value.bin; // PR_SEARCH_KEY from the profile 
      rgProps[1].ulPropTag = PR_MESSAGE_CLASS; 
      rgProps[1].Value.LPSZ = (LPTSTR)"IPM.MessageManager";
   ```

4. 表から **、IMAPITable::FindRow を使用して非表示のメッセージを検索します**。
    
5. 手順 4 で非表示のメッセージが見つからなくなった場合は、以下に示すように **、PidTagConversationKey** の代わりに **PidTagSearchKey** (**PR_SEARCH_KEY**) を使用する制限を変更します。
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. **IMAPITable::FindRow を使用して非表示のメッセージを検索します**。 
    
7. 手順 6 に失敗した場合は [、PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) を使用する制限を次の値に変更します (以下に、簡単にスタイル置換を使用します  `printf` )。 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. **IMAPITable::FindRow を使用して非表示のメッセージを検索します**。
    
9. 2010 Outlook 以降のバージョンを実行している場合は **、PidTagProfileName** ( PR_PROFILE_NAME ) と **PidTagSearchKey** ( PR_SEARCH_KEY ) にそれぞれ次の **値を** 使用します。
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   手順 3 ~ 8 を実行します。 メッセージの検索に失敗した場合は、元の手順 3 ~ 8 に戻ります。
    
10. 手順 4、6、または 8 で見つかった非表示のメッセージを開きます。

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>非表示のメッセージの適切な添付ファイルを検索する

非表示のメッセージには複数の添付ファイルが含まれますので、次の順序で適切な添付ファイルを探します。
  
> [!NOTE]
> この手順では、再びスタイル  `printf` 置換を使って簡単に行います。 

1. [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) が、ユーザーのプロファイルで指定されているユーザーの SMTP アドレスである次の文字列と一致する添付ファイルを `szEmailAddress` 探します。 . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) **(** PR_ATTACH_FILENAME ) が "BlobPOP%s" と一致する添付ファイルを探します `szEmailAddress` 。
    
3. [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) **(** PR_DISPLAY_NAME ) が "BlobPOP%s" と一致する添付ファイルを探します `szEmailAddress` 。
    
4. **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) が "Blob%8x" と一致する添付ファイルを探します。このファイルは、PROP_ACCT_MINI_UID `dwAcctUID` `dwAcctUID` から [取得されます](prop_acct_mini_uid.md)。 [IOlkAccount::GetProp](iolkaccount-getprop.md)メソッドを使用して、PROP_ACCT_MINI_UIDできます **。** 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>メッセージ添付ファイルの PidTagAttachDataBinary プロパティにアクセスする

非表示メッセージの適切なメッセージ添付ファイルを見つけると **、IMAPIProp::GetProps** を使用して添付ファイルの **PidTagAttachDataBinary** プロパティを読み取ります。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>次の手順

このトピックでは、POP3 メール クライアントの受信トレイのメッセージダウンロード履歴を見つける方法について説明しました。 受信 [トレイ用にダウンロードまたは](parsing-the-message-download-history-for-a-pop3-account.md) 削除されたメッセージを識別するために、この履歴を解析する方法については、「POP3 アカウントのメッセージダウンロード履歴の解析」を参照してください。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)   
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
- [POP3 UIDL 履歴の検索](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

