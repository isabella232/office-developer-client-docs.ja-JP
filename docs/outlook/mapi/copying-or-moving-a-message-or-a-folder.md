---
title: メッセージまたはフォルダーのコピーまたは移動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年 11 月 08 日'
ms.openlocfilehash: c06fee83d217339d48d66963a721143c9d26e25b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567733"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>メッセージまたはフォルダーのコピーまたは移動
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、次の 4 つの方法のいずれかを使用して、メッセージまたはフォルダーをコピーまたは移動できます。
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
適切なフラグとパラメーターを設定することで **、CopyTo** と **CopyProps** を **CopyFolder** や CopyMessages と同じ方法 **で動作できます**。 呼び出すメソッドを決定する際には、次の問題を考慮してください。
  
- フォルダーまたはメッセージをコピーまたは移動していますか?
    
- 移動またはコピーするフォルダーまたはメッセージについてどのくらい知っていますか?
    
- 移動またはコピーされるフォルダーまたはメッセージのプロパティの数。
    
**IMAPIProp** メソッドを使用して、フォルダーまたはメッセージをコピーまたは移動できます。 **IMAPIFolder::CopyMessages はメッセージ** でのみ動作します。 **IMAPIFolder::CopyFolder は** フォルダーでのみ動作します。 
  
**IMAPIFolder** メソッドを使用しても、コピーまたは移動するフォルダーまたはメッセージでサポートされるプロパティに関する知識は必要ないのに対し **、IMAPIProp** メソッドを使用するにはいくつかの知識が必要です。 **IMAPIProp::CopyProps** では、コピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。 **IMAPIProp::CopyTo** では、すべてのプロパティをコピーまたは移動する場合を除き、除外するプロパティを明示的に指定する必要があります。 これらのメソッドの詳細については [、「COPYing MAPI プロパティ」を参照してください](copying-mapi-properties.md)。
  
コピーまたは移動するプロパティの数は、使用するメソッドに関する決定に影響を与える可能性があります。 複数のメッセージをコピーまたは移動する場合は **、IMAPIFolder::CopyMessages を呼び出します**。 別の選択肢として **、IMAPIProp::CopyProps** を呼び出して、フォルダーのプロパティ [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)プロパティPR_CONTAINER_CONTENTSのみをコピーします。 次の手順は **、CopyMessages を使用する方法を示しています**。 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>1 つ以上のメッセージをコピーまたは移動するには
  
1. ソース フォルダーと移動先フォルダーの有効なエントリ識別子を見つける。
    
2. [IMAPISession::OpenEntry](imapisession-openentry.md)または[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出し、MAPI_MODIFY フラグを設定して、これらのフォルダーを読み取り/書き込みモードで開きます。 
    
3. **OpenEntry** から返されるインターフェイス ポインターが **IMAPIFolder インターフェイス ポインターである必要** があります。 指定しない場合は、LPMAPIFOLDER 型にキャストします。 
    
4. コピーまたは移動する 1 つ以上のメッセージを表すエントリ識別子の配列を作成します。 
    
5. 次 **のフラグを設定して IMAPIFolder::CopyMessages** を呼び出します。 
    
   - MESSAGE_MOVE操作を実行する場合は、次の操作を実行します。 
    
   - MESSAGE_DIALOG進行状況インジケーターを表示する場合は  _、ulUIParam_ パラメーターでウィンドウ ハンドルを取得して渡します。 
    
6. ソース フォルダー **と移動先フォルダーの IMAPIFolder** ポインターを解放します。 
    
フォルダーの完全な内容を別のフォルダーにコピーする場合は、ソース フォルダーの **IMAPIFolder::CopyFolder** または **IMAPIProp::CopyTo** メソッドを呼び出します。 
  
フォルダーのプロパティの一部をコピーするには **、IMAPIProp::CopyProps メソッドを呼び出** します。 フォルダーのプロパティのほとんどをコピーするには **、IMAPIProp::CopyTo を呼び出します**。 
  
たとえば、フォルダーの **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティと PR_COMMENT ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティをコピーする場合、次のオプションがあります。 
  
- **IMAPIFolder::CopyFolder** を呼び出して、すべてのフォルダー プロパティをコピーし、新しいフォルダーから不要なプロパティを削除します。 
    
- **CopyTo を呼び** 出し、フォルダーとフォルダーのプロパティを除くすべてのPR_DISPLAY_NAME **を** PR_COMMENT。 
    
- **CopyProps を呼** び出し、include **PR_DISPLAY_NAME****内PR_COMMENT** を渡します。 
    
この場合、プロパティの小さなセットをコピーするために使用することを意図し、実装する最も簡単な呼び出しなので **、CopyProps** が最適です。 
  
メッセージを含めずにフォルダー プロパティのみをコピーまたは移動するには、フォルダーの **IMAPIProp::CopyTo** メソッドを呼び出し、次のプロパティを除外します。 
  
- **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
copy メソッドは、成功、成功S_OK、部分的な成功MAPI_W_PARTIAL_COMPLETIONエラーを示すデータを返します。 エラー MAPI_W_PARTIAL_COMPLETION場合は、HR_FAILED **マクロを** 使用して、より具体的なエラーにアクセスします。 詳細については、「Using [Macros for Error Handling 」を参照してください](using-macros-for-error-handling.md)。
  
あるメッセージ ストアから別のメッセージ ストアにメッセージをコピーし、Unicode が両方でサポートされていない場合は、コード ページ変換によって情報が失われる可能性があります。 通常、メッセージ ストアが一方または両方の形式をサポートするかどうかはわかりません。そのため、テキスト プロパティを ASCII 文字列としてコピーするか、Unicode 文字列としてコピーするかは判断できません。 Unicode をサポートしている場合は、Unicode コピーを実行してみてください。エラー値を使用してエラーが発生した場合MAPI_E_BAD_CHARWIDTH ASCII を使用します。
  

