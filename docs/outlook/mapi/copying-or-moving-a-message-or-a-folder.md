---
title: コピーまたはメッセージまたはフォルダーを移動します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年 11 月 8 日'
ms.openlocfilehash: 26fe135da93e0f5f94d9f7d264453b74f97a518b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799856"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>コピーまたはメッセージまたはフォルダーを移動します。
  
**適用対象**: Outlook 
  
クライアントは、コピーまたはメッセージまたはフォルダーを移動する 4 つの方法のいずれかを使用できます。
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
適切なフラグとパラメーターを設定することにより**CopyTo**と**CopyProps**が動作するように**CopyFolder**または**CopyMessages**のようにします。 どのメソッドを呼び出すを決定する際に、次の問題を考慮してください。
  
- コピーまたは、フォルダーまたはメッセージを移動しますか。
    
- どの程度ご存知のフォルダーまたはメッセージを移動またはコピーできるのですか。
    
- フォルダーの数や、メッセージのプロパティを移動またはコピーされますか。
    
**IMAPIProp**メソッドは、コピーまたは移動するフォルダーまたはメッセージのいずれかを使用できます。 **IMAPIFolder::CopyMessages**は、メッセージだけです。**IMAPIFolder::CopyFolder**は、フォルダーにのみで動作します。 
  
**IMAPIFolder**メソッドを使用してもフォルダーまたはメッセージをコピーまたは移動によってサポートされるプロパティのすべての知識が必要ありませんが、 **IMAPIProp**メソッドを使用するいくつかの知識が必要です。 **IMAPIProp::CopyProps**とのコピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。 **IMAPIProp::CopyTo**、コピーまたは移動するすべてのプロパティ、する場合を除き、明示的に指定してくださいどれを除外する必要があります。 これらのメソッドの詳細については、 [MAPI プロパティのコピー](copying-mapi-properties.md)を参照してください。
  
コピーまたは移動するプロパティの数は、使用する方法の決定に影響を与えます。 コピーまたは複数のメッセージを移動する場合は、 **IMAPIFolder::CopyMessages**を呼び出します。 代替の選択肢は、フォルダーの**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) のプロパティだけをコピーするのには**IMAPIProp::CopyProps**を呼び出すことです。 次の手順では、 **CopyMessages**を使用する方法を示します。 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>コピーまたは 1 つまたは複数のメッセージを移動するには
  
1. 元とコピー先のフォルダーの有効なエントリの識別子を検索します。
    
2. [IMAPISession::OpenEntry](imapisession-openentry.md)または[IMsgStore::OpenEntry](imsgstore-openentry.md)のいずれかを呼び出すと、MAPI_MODIFY フラグを設定して、読み取り/書き込みモードでこれらのフォルダーを開きます。 
    
3. **OpenEntry**から返されたインターフェイス ポインターが**IMAPIFolder**インターフェイス ポインターであることを確認します。 いない場合は、LPMAPIFOLDER 型にキャストします。 
    
4. コピーまたは移動する 1 つまたは複数のメッセージを表すエントリの識別子の配列を作成します。 
    
5. 次のフラグのセットを使用して**IMAPIFolder::CopyMessages**を呼び出します。 
    
   - 移動操作を実行する場合は、MESSAGE_MOVE です。 
    
   - MESSAGE_DIALOG とウィンドウのパスは、 _ulUIParam_パラメーターに処理する場合は、進行状況インジケーターを表示するフォルダー。 
    
6. 元とコピー先のフォルダーの**IMAPIFolder**のポインターを解放します。 
    
別のフォルダーにフォルダーの内容全体をコピーする場合は、元のフォルダーの**IMAPIFolder::CopyFolder**または**IMAPIProp::CopyTo**メソッドを呼び出します。 
  
フォルダーのプロパティの一部をコピーするには、 **IMAPIProp::CopyProps**メソッドを呼び出します。 ほとんどのフォルダーのプロパティをコピーするには、 **IMAPIProp::CopyTo**を呼び出します。 
  
たとえば、フォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) のプロパティをコピーする場合は、次のオプションがあります。
  
- フォルダーのプロパティのすべてをコピーし、新しいフォルダーから不要なエントリを削除するのには**IMAPIFolder::CopyFolder**を呼び出します。 
    
- **CopyTo**を呼び出すし、すべての**PR_DISPLAY_NAME**と**PR_COMMENT**以外のフォルダーのプロパティを除外します。 
    
- **CopyProps**、 **PR_DISPLAY_NAME**と**PR_COMMENT**を含む配列に渡してを呼び出します。 
    
この例では、 **CopyProps**に最適な選択肢小さいプロパティのセットをコピーするためにするものですのでを実装する最も簡単な呼び出し。 
  
コピーまたはメッセージを含めずに、フォルダーのプロパティのみを移動、フォルダーの**IMAPIProp::CopyTo**メソッドを呼び出すし、次のプロパティを除外します。 
  
- **PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
コピー メソッドは S_OK を MAPI_W_PARTIAL_COMPLETION、完全な成功を示す部分的な成功またはエラーを示すを返すことができます。 MAPI_W_PARTIAL_COMPLETION が返された場合より詳細なエラーにアクセスする**HR_FAILED**マクロを使用します。 詳細については、[エラーを処理するためのマクロの使用](using-macros-for-error-handling.md)を参照してください。
  
両方では、Unicode はサポートされていない別の 1 つのメッセージ ストアからメッセージをコピーする場合は、情報がコード ページ変換が失われることに注意します。 通常かわからないかどうか、メッセージ ・ ストアは、1 つまたは両方の形式をサポートとして ASCII 文字列または Unicode 文字列としてのテキストのプロパティをコピーするかどうかを判断することが不可能になります。 Unicode をサポートする場合は、実行しようと Unicode のコピーです。エラー値 MAPI_E_BAD_CHARWIDTH で失敗した場合、ASCII に頼る。
  

