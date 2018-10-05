---
title: POP3 アカウントのメッセージ ダウンロード履歴の検索
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: このトピックでは、メール クライアントが POP3 アカウントのメッセージのダウンロードの履歴を取得する PidTagAttachDataBinary プロパティにアクセスする方法について説明します。
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399558"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の検索

このトピックでは、メール クライアントが POP3 アカウントのメッセージのダウンロードの履歴を取得する[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティにアクセスする方法について説明します。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>理由メッセージ ダウンロードの履歴を取得しますか。

Outlook の Post Office プロトコル (POP) プロバイダーを取得し、ローカル デバイス上の新しい電子メール メッセージをダウンロードしてその後に残すかメール サーバー上のこれらの電子メール メッセージを削除できます。 メール クライアントは、ダウンロードする新しいメッセージをチェックし、識別し、その受信トレイの新着メッセージのみをダウンロードできるようにする必要があります。 メール クライアントは、最初の一意の識別子 (UID)、その受信トレイに配信されたことを各メッセージ マップを取得する (一意な ID を一覧表示) UIDL コマンドを使用します。 クライアントは、ダウンロードまたはそのクライアントの受信トレイで削除されたメッセージのメッセージのダウンロードの履歴を取得します。 メッセージ マップの UID とダウンロードの履歴を使用して、クライアントことができますし、メッセージを識別するそれらは存在しない新規となり、履歴をダウンロードする必要があります。
  
受信トレイのメッセージのダウンロードの履歴を取得します。
  
- 特定の形式に依存するバイナリ ラージ オブジェクト (BLOB) の履歴が含まれています、 **PidTagAttachDataBinary**プロパティを検索するには、このトピックの手順を実行します。 
    
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)では、ダウンロードまたは削除する受信トレイのメッセージを識別するには、この BLOB を解析する方法について説明するを続行します。
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>ダウンロード履歴の確認メッセージを検索するための中核となる概念

受信トレイのメッセージのダウンロードの履歴は、バイナリ MAPI プロパティ、 **PidTagAttachDataBinary**、受信トレイ内の非表示メッセージの添付ファイルに格納されます。 表 1 は、メッセージを検索する方法を理解するのに役立ちますが履歴をダウンロードすることの概念のためのリソースを示しています。
  
**表 1. 中心概念**

|**記事のタイトル**|**説明**|
|:-----|:-----|
|[��\���ɂ��� MAPI �t�H���_�[](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI では、フォルダーを非表示と非表示メッセージで情報を格納するメール クライアントを使用できます。 隠しフォルダーが MAPI フォルダーの関連する部分では、通常に表示されていない情報が含まれてし、ユーザが操作します。 クライアントでは、フォーマットと隠しフォルダーを非表示のメッセージに格納する内容を決定します。  <br/> |
|[MAPI メッセージ](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI では、いずれかのユーザーがクライアント、またはサブツリー以外でユーザーを非表示に表示されている標準の IPM サブツリー内のフォルダーにメッセージを格納します。 メッセージには、追加のデータ ファイル、もう 1 つのメッセージ、または OLE オブジェクトの形式では、添付ファイルに格納されていることができます。 メッセージ ダウンロードの履歴] の場合は、履歴は、別の非表示メッセージに添付されているメッセージのプロパティに格納されます。  <br/> |
|[メッセージ プロパティの概要](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |クライアントは、メッセージで情報を保存するとき実際には、メッセージのプロパティに情報を格納します。 MAPI には、多くのプロパティがサポートされています-は、いくつかが常に存在し、クライアントで設定することができます-クライアントは利用できないか、設定することはできないと有効な値にします。 メッセージのダウンロードの履歴は、非表示メッセージの添付ファイルの**PidTagAttachDataBinary**プロパティに格納されます。  <br/> |
|[MAPI プロファイル](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |セッションでログオン時に、メール クライアントは、使用するプロバイダーとサービスを記述するプロファイルを選択します。 プロファイルは、プロパティを含むセクションに分かれています。 具体的には、 [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) と[PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) プロパティ常に存在します。 プロファイルの検索キーはすべてのプロファイルでは、一意であり、 **MUID_PROFILE_INSTANCE** (MAPIGUID で定義されますこれによって識別されるプロファイル セクションに保存されます。H を参照)。 [IMAPISession::OpenProfileSection](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx)を使用して、セクションを開くし、 [IMAPIProp::GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)を使用してプロパティ値を取得します。  <br/> |
|[コンテンツ テーブル](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |メッセージ ストア プロバイダーは、そのフォルダーの内容テーブルを実装します。 フォルダーの関連する部分での非表示メッセージのメッセージ ストア プロバイダーが、関連付けられている内容のテーブルをサポートし、クライアントはコンテンツが関連付けられているテーブルにポインターを返す[IMAPIContainer::GetContentsTable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx)メソッドを使用することができます。  <br/> |
|[制限について](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [制限の種類](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [制限の作成](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [制限のサンプル コード](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |MAPI クライアントを特定の値に設定されて、特定のプロパティを持つメッセージを表す行を検索し、内容のテーブルにフィルターを適用するのに制限を使用できます。 制限を定義するより専門的な制限の構造体の共用体を含めることができるデータ構造体[SRestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx)を使用します。 [IMAPITable::FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx)メソッドでは、制限を適用し、制限の条件に一致するテーブルの最初の行を取得します。  <br/> |
|[インデックス作成のためのストア登録について](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |[PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) プロパティを使用すると、ストア プロバイダーの種類を確認します。 たとえば、ストアが Exchange ストアかどうかを確認するに、 **PidTagStoreProvider**プロパティは、定数**pbExchangeProviderPrimaryUserGuid**、パブリック ヘッダー ファイルの edkmdb.h で定義されているで表される値を返す必要があります。  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>適切な非表示のメッセージと添付ファイルを検索します。

わかったところで、受信トレイのメッセージのダウンロードの履歴が非表示のメッセージの添付ファイルの**PidTagAttachDataBinary**プロパティには、適切な非表示メッセージの適切な添付ファイルを検索する手順は、以下手順です。 
  
1. [適切な非表示のメッセージを検索します。](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [非表示メッセージの適切な添付ファイルを検索します。](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスします。](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>適切な非表示のメッセージを検索します。

1. **MUID_PROFILE_INSTANCE**で指定されたプロファイル] セクションで、プロファイルの[PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) プロパティを取得します。
    
2. **IMAPIContainer::GetContentsTable**を呼び出すことによって、受信トレイ フォルダーに関連付けられているコンテンツを開きます。
    
3. [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**)、 **PidTagSearchKey** (**PR_SEARCH_KEY**) および[PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) のプロパティに基づいて制限を作成するテーブルを取得します。非表示すべてのメッセージに関連付けられている受信トレイの内容が含まれています。 次に、 [POP3 UIDL 履歴を検索する](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)から抽出される制限の例を示します。
    
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

4. テーブルからは、 **IMAPITable::FindRow**を使用して非表示のメッセージを検索します。
    
5. 手順 4 では、非表示メッセージを検索する失敗した場合、次のように、 **PidTagConversationKey**、代わりに**PidTagSearchKey** (**PR_SEARCH_KEY**) を使用する制限を変更します。
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. **IMAPITable::FindRow**を使用して非表示のメッセージを検索します。 
    
7. ステップ 6 が失敗した場合、 [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**あるの PR_SUBJECT**)、次の値に等しくなるを使用する制限を変更する (を使用して次に示す`printf`簡潔にするための代替のスタイルを設定) します。 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. **IMAPITable::FindRow**を使用して非表示のメッセージを検索します。
    
9. Outlook 2010 またはそれ以降のバージョンを実行している場合、それぞれ**PidTagProfileName** (**PR_PROFILE_NAME**) と**PidTagSearchKey** (**PR_SEARCH_KEY**) の次の値を使用します。
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   3 ~ 8 の手順を実行します。 メッセージを検索するのにはこれが失敗した場合は、元の手順 3 ~ 8 に戻る。
    
10. 4、6、または 8 の手順で見つかった非表示メッセージを開きます。

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>非表示メッセージの適切な添付ファイルを検索します。

非表示のメッセージは、複数の添付ファイルを必要があります、ためには、次の順序で適切な添付ファイルを検索します。
  
> [!NOTE]
> この手順をもう一度使用して、`printf`簡潔にするための代替のスタイルを設定します。 

1. [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) が次の文字列と一致する添付ファイルを探して、`szEmailAddress`は、ユーザーの SMTP アドレスでは、ユーザーのプロファイルで指定されています。 . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**)"BlobPOP: %s"に一致する添付ファイルの`szEmailAddress`。
    
3. [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**)"BlobPOP: %s"に一致する添付ファイルの`szEmailAddress`。
    
4. **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) が"Blob%.8x"と一致する添付ファイルを検索`dwAcctUID`、 `dwAcctUID` [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)に由来します。 **PROP_ACCT_MINI_UID**プロパティにアクセスするのには、 [IOlkAccount::GetProp](iolkaccount-getprop.md)メソッドを使用することができます。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスします。

非表示メッセージの適切なメッセージの添付ファイルを検索するには後に、、添付ファイルの**PidTagAttachDataBinary**プロパティに**IMAPIProp::GetProps**を使用します。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>次の手順

このトピックは、POP3 メール クライアントの受信トレイのメッセージのダウンロードの履歴を検索する方法を学習しました。 ダウンロードまたは受信トレイで削除されたメッセージを識別するには、この履歴を解析する方法については、 [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)を参照してください。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)   
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
- [POP3 UIDL 履歴を検索します。](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

