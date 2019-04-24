---
title: POP3 アカウントのメッセージ ダウンロード履歴の検索
manager: soliver
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 90a51150-5c2c-4d5b-8717-5dacc8532744
description: このトピックでは、メールクライアントが PidTagAttachDataBinary プロパティにアクセスして、POP3 アカウントのメッセージのダウンロード履歴を取得する方法について説明します。
ms.openlocfilehash: ae12a044098aa4f42e1c2e5936e82da3d7a128dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321876"
---
# <a name="locating-the-message-download-history-for-a-pop3-account"></a>POP3 アカウントのメッセージ ダウンロード履歴の検索

このトピックでは、メールクライアントが[PidTagAttachDataBinary](https://msdn.microsoft.com/library/3b0a8b28-863e-4b96-a4c0-fdb8f40555b9%28Office.15%29.aspx)プロパティにアクセスして、POP3 アカウントのメッセージのダウンロード履歴を取得する方法について説明します。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_WhyGetUIDLHistory"> </a>

## <a name="why-get-the-message-download-history"></a>メッセージのダウンロード履歴を取得する理由

Outlook の Post Office Protocol (POP) プロバイダーを使用すると、ユーザーは新しい電子メールメッセージをローカルデバイスで取得してダウンロードし、メールサーバー上でこれらの電子メールメッセージを残すか削除することができます。 メールクライアントは、新しいメッセージのダウンロードを確認するときに、その受信トレイの新しいメッセージのみを識別してダウンロードできる必要があります。 メールクライアントはまず、UIDL (一意の ID リスト) コマンドを使用して、その受信トレイに配信された各メッセージのマップを一意の識別子 (UID) に取得します。 クライアントは、そのクライアント上で受信トレイに対してダウンロードまたは削除されたメッセージのメッセージダウンロード履歴も取得します。 メッセージ UID マップとダウンロード履歴を使用して、クライアントは履歴内に存在しないメッセージを新規として識別できるため、ダウンロードする必要があります。
  
受信トレイのメッセージダウンロード履歴を取得するには、次のようにします。
  
- このトピックの手順に従って**PidTagAttachDataBinary**プロパティを検索します。これには、特定の形式に従ったバイナリラージオブジェクト (BLOB) 内の履歴が含まれます。 
    
- 次に、 [POP3 アカウントのメッセージダウンロード履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)を続けます。この BLOB を解析して、その受信トレイでダウンロードまたは削除されたメッセージを識別する方法について説明します。
    
## <a name="core-concepts-to-know-for-locating-the-message-download-history"></a>メッセージのダウンロード履歴を検索する際に知っておく必要がある中心概念

受信トレイのメッセージのダウンロード履歴は、受信トレイ内の非表示のメッセージの添付ファイルにある**PidTagAttachDataBinary**というバイナリ MAPI プロパティに格納されます。 表1は、メッセージのダウンロード履歴を見つける方法を理解するのに役立つ概念のリソースを示しています。
  
**表 1. 中心概念**

|**記事のタイトル**|**説明**|
|:-----|:-----|
|[MAPI の隠しフォルダー](https://msdn.microsoft.com/library/8b3b9c80-f7f4-4f37-bd6b-323469d020f1%28Office.15%29.aspx) <br/> |MAPI では、メールクライアントが非表示のフォルダーおよび非表示のメッセージに情報を格納することができます。 隠しフォルダーは MAPI フォルダーの関連部分にあり、通常、ユーザーが操作することはできず、表示されない情報が含まれています。 クライアントは、隠しメッセージに隠しフォルダーに格納するための形式と内容を決定します。  <br/> |
|[MAPI メッセージ](https://msdn.microsoft.com/library/417c113f-bd98-4515-85d1-09db7fc3a227%28Office.15%29.aspx) <br/> |MAPI は、クライアントのユーザーに対して表示される標準の IPM サブツリー、またはサブツリーの外部にあるフォルダーにメッセージを格納し、ユーザーには見えません。 メッセージには添付ファイルに格納される追加のデータを含めることができます。これは、ファイル、別のメッセージ、または OLE オブジェクトの形式にすることができます。 メッセージのダウンロード履歴の場合、履歴は別の非表示メッセージに添付されたメッセージのプロパティに格納されます。  <br/> |
|[メッセージプロパティの概要](https://msdn.microsoft.com/library/447f54de-9f0d-4f73-89b6-bed9cfea9c15%28Office.15%29.aspx) <br/> |クライアントは、メッセージに情報を格納するときに、実際にはメッセージのプロパティに情報を格納します。 MAPI は多くのプロパティをサポートしています。一部は常に存在し、クライアントによって設定できます。その他はオプションであり、クライアントはそれらを利用できない、または有効な値に設定することを想定できません。 メッセージのダウンロード履歴は、非表示のメッセージの添付ファイルの**PidTagAttachDataBinary**プロパティに格納されます。  <br/> |
|[MAPI プロファイル](https://msdn.microsoft.com/library/493c87a4-317d-47ec-850b-342cac59594b%28Office.15%29.aspx) <br/> |セッションのログオン時に、メールクライアントは、使用するプロバイダーとサービスを記述するプロファイルを選択します。 プロファイルは、プロパティを含むセクションに分かれています。 特に、 [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) および[PidTagProfileName](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx) (**PR_PROFILE_NAME**) プロパティは常に存在します。 プロファイルの検索キーは、すべてのプロファイルで一意であり、 **MUID_PROFILE_INSTANCE**によって識別されるプロファイルセクションに格納されます (mapiguid で定義されています)。H)。 [imapisession:: openプロファイル](https://msdn.microsoft.com/library/e2757028-27e7-4fc0-9674-e8e30737ef1d%28Office.15%29.aspx)を使用してセクションを開き、 [imapisession:: GetProps](https://msdn.microsoft.com/library/1c7a9cd2-d765-4218-9aee-52df1a2aae6c%28Office.15%29.aspx)を使用してプロパティ値を取得します。  <br/> |
|[目次テーブル](https://msdn.microsoft.com/library/7b8efb4e-b5be-41b8-81bb-9aa1da421433%28Office.15%29.aspx) <br/> |メッセージストアプロバイダーは、フォルダーのコンテンツテーブルを実装します。 フォルダーの関連部分に含まれる非表示のメッセージの場合、メッセージストアプロバイダーは関連付けられたコンテンツテーブルをサポートし、クライアントは[IMAPIContainer:: getcontentstable](https://msdn.microsoft.com/library/88c7a666-875d-473a-b126-dbbb7009f7d9%28Office.15%29.aspx)メソッドを使用して、関連付けられた contents テーブルへのポインターを返します。  <br/> |
|[制限について](https://msdn.microsoft.com/library/e119fa20-08b8-4c8d-93fc-56037220890d%28Office.15%29.aspx) <br/> [制限の種類](https://msdn.microsoft.com/library/0d3bd58b-7100-4117-91ac-27139715c85b%28Office.15%29.aspx) <br/> [制限の作成](https://msdn.microsoft.com/library/12abbd8c-f825-493e-af42-344371d9658e%28Office.15%29.aspx) <br/> [制限コードの例](https://msdn.microsoft.com/library/9b82097c-dbd6-4ba0-a6cb-292301f9402b%28Office.15%29.aspx) <br/> |MAPI では、クライアントは、コンテンツテーブルのフィルター処理に制限を使用して、特定のプロパティが特定の値に設定されているメッセージを表す行を検索できます。 制限は、 [srestriction](https://msdn.microsoft.com/library/c12b4409-da6f-480b-87af-1e5baea2e8bd%28Office.15%29.aspx)データ構造を使用して定義されます。これには、さらに特殊な制限構造の和集合を含めることができます。 [IMAPITable:: FindRow](https://msdn.microsoft.com/library/6511368c-9777-497e-9eea-cf390c04b92e%28Office.15%29.aspx)メソッドは、制限を適用し、制限条件に一致するテーブルの最初の行を取得します。  <br/> |
|[インデックス作成のためのストア登録について](https://msdn.microsoft.com/library/dd2aa06a-96e8-1291-18b5-fc3c40b74e4d%28Office.15%29.aspx) <br/> |[PidTagStoreProvider](https://msdn.microsoft.com/library/6f6cc66f-a08e-4f8e-b33a-d3674319248e%28Office.15%29.aspx) (**PR_MDB_PROVIDER**) プロパティを使用して、ストアプロバイダーの種類を確認します。 たとえば、ストアが Exchange ストアであるかどうかを確認するには、 **PidTagStoreProvider**プロパティは、パブリックヘッダーファイル edkmdb で定義されている定数**pbexchangeproviderprimaryuserguid**で表される値を返す必要があります。  <br/> |
   
## <a name="locating-the-appropriate-hidden-message-and-attachment"></a>適切な非表示メッセージと添付ファイルを特定する

受信トレイのメッセージのダウンロード履歴が非表示メッセージへの添付ファイルの**PidTagAttachDataBinary**プロパティに含まれていることがわかったので、該当する非表示メッセージの適切な添付ファイルを特定するには、次の手順を実行します。ここ 
  
1. [適切な非表示メッセージを見つける](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg)
    
2. [非表示メッセージの適切な添付ファイルを検索する](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment)
    
3. [メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスする](#OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp)

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindHiddenMsg"> </a>

### <a name="find-the-appropriate-hidden-message"></a>適切な非表示メッセージを見つける

1. プロファイルから、 **MUID_PROFILE_INSTANCE**で指定されたプロファイルセクションの[PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) (**PR_SEARCH_KEY**) プロパティを取得します。
    
2. **IMAPIContainer:: getcontentstable**を呼び出して、受信トレイフォルダーに関連付けられているコンテンツを開きます。
    
3. [PidTagConversationKey](https://msdn.microsoft.com/library/52c97d6c-7f4b-4522-aeac-0c1ed8475952%28Office.15%29.aspx) (**PR_CONVERSATION_KEY**)、 **PidTagSearchKey** (**PR_SEARCH_KEY**)、および[PidTagMessageClass](https://msdn.microsoft.com/library/1e704023-1992-4b43-857e-0a7da7bc8e87%28Office.15%29.aspx) (**PR_MESSAGE_CLASS**) の各プロパティに基づいて制限を作成し、テーブルを取得します。受信トレイの関連コンテンツのすべての非表示メッセージを含みます。 次に示すのは、 [POP3 UIDL 履歴の検索](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)から抽出される制限の例です。
    
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

4. 表から、 **IMAPITable:: FindRow**を使用して隠しメッセージを検索します。
    
5. 非表示メッセージの検索に失敗した場合は、次のように、 **PidTagSearchKey** (**PR_SEARCH_KEY**) を**PidTagConversationKey**の代わりに使用するように制限を変更します。
    
   ```cpp
    rgRes[1].res.resProperty.ulPropTag = rgProps[0].ulPropTag = PR_SEARCH_KEY;
   ```

6. **IMAPITable:: FindRow**を使用して、隠しメッセージを検索します。 
    
7. 手順6でエラーが発生した場合は、 [PidTagSubject](https://msdn.microsoft.com/library/aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9%28Office.15%29.aspx) (**PR_SUBJECT**) を使用するように制限を変更し`printf` 、次の値と等しくなるようにします (以下にスタイル置換を使用して簡潔に説明します)。 
    
   ```cpp
    "Outlook Message Manager (%s) (KEY: %s)", PR_PROFILE_NAME, HexFromBin(PR_SEARCH_KEY)
   ```

8. **IMAPITable:: FindRow**を使用して、隠しメッセージを検索します。
    
9. Outlook 2010 またはそれ以降のバージョンを実行している場合は、 **PidTagProfileName** (**PR_PROFILE_NAME**) および**PidTagSearchKey** (**PR_SEARCH_KEY**) にそれぞれ次の値を使用します。
    
   ```cpp
    CHAR g_szGeneralKey[] = "General Key"; 
    const SBinary g_binGeneralKey = {sizeof(g_szGeneralKey), (LPBYTE)g_szGeneralKey};
   ```

   手順 3 ~ 8 を実行します。 これでメッセージの検索に失敗した場合は、元の手順 3 ~ 8 に戻ります。
    
10. 手順4、6、または8で見つかった非表示のメッセージを開きます。

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_FindAttachment"> </a>

### <a name="find-the-appropriate-attachment-of-the-hidden-message"></a>非表示メッセージの適切な添付ファイルを検索する

非表示のメッセージには複数の添付ファイルがある場合があるので、次の順序で該当する添付ファイルを探します。
  
> [!NOTE]
> この手順を実行する`printf`と、簡潔にするためにスタイルの代替が使用されます。 

1. [PidTagAttachLongFilename](https://msdn.microsoft.com/library/83b69e8f-0b5a-4992-b5b8-160d3bdfa22a%28Office.15%29.aspx) (**PR_ATTACH_LONG_FILENAME**) が次の文字列と一致する添付ファイルを検索`szEmailAddress`します。ここで、はユーザーのプロファイルに指定されたユーザーの SMTP アドレスです。 . 
    
   ```cpp
    "BlobPOP%s", szEmailAddress
   ```

2. [PidTagAttachFilename](https://msdn.microsoft.com/library/cbf34dd6-7733-47f6-9c41-9d82656ca9dc%28Office.15%29.aspx) (**PR_ATTACH_FILENAME**) が "blobpop% s" と一致する添付ファイルを`szEmailAddress`探します。
    
3. [PidTagDisplayName](https://msdn.microsoft.com/library/bd094e00-5c60-4bb3-9a45-b943fab52876%28Office.15%29.aspx) (**PR_DISPLAY_NAME**) が "blobpop% s" と一致する添付ファイルを`szEmailAddress`探します。
    
4. **PidTagAttachFilename** (**PR_ATTACH_FILENAME**) が "Blob% .8x" `dwAcctUID`と一致する添付ファイルを検索します`dwAcctUID` 。ここで、は[PROP_ACCT_MINI_UID](prop_acct_mini_uid.md)からのものです。 **PROP_ACCT_MINI_UID**プロパティにアクセスするには、 [IOlkAccount:: getprop](iolkaccount-getprop.md)メソッドを使用します。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AccessProp"> </a>

### <a name="access-the-pidtagattachdatabinary-property-of-the-message-attachment"></a>メッセージの添付ファイルの PidTagAttachDataBinary プロパティにアクセスする

非表示メッセージの適切なメッセージ添付ファイルを特定した後、 **imapiprop:: GetProps**を使用して添付ファイルの**PidTagAttachDataBinary**プロパティを読み取ります。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_NextSteps"> </a>

## <a name="next-steps"></a>次の手順

このトピックでは、POP3 メールクライアントの受信トレイのメッセージダウンロード履歴を見つける方法について説明しました。 この履歴を解析して、受信トレイでダウンロードまたは削除されたメッセージを識別する方法については、「 [POP3 アカウントのメッセージダウンロード履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)」を参照してください。 

<a name="OL15Con_AuxRef_LocatingMsgsUIDLHistory_AdditionalRsc"> </a>

## <a name="see-also"></a>関連項目

- [POP3 アカウントのメッセージ ダウンロードの管理](managing-message-downloads-for-pop3-accounts.md)   
- [POP3 アカウントのメッセージのダウンロードの履歴の解析](parsing-the-message-download-history-for-a-pop3-account.md)
- [POP3 の UIDL の履歴を見つける](https://blogs.msdn.com/b/stephen_griffin/archive/2012/12/03/locating-the-pop3-uidl-history.aspx)
    

