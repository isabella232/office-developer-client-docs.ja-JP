---
title: メッセージまたはフォルダーのコピーまたは移動
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: '最終更新日: 2011 年11月8日'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413501"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a>メッセージまたはフォルダーのコピーまたは移動
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは、次の4つの方法のいずれかを使用して、メッセージまたはフォルダーをコピーまたは移動できます。
  
- [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
- [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
- [IMAPIProp::CopyTo](imapiprop-copyto.md)
    
- [IMAPIProp::CopyProps](imapiprop-copyprops.md)
    
適切なフラグとパラメーターを設定することによって、 **CopyTo**および copyprops を**copyprops**や**** **copyprops**と同じように動作させることができます。 呼び出すメソッドを決定するときは、以下の点を考慮してください。
  
- フォルダーまたはメッセージをコピーまたは移動していますか。
    
- 移動またはコピーするフォルダーまたはメッセージについて、どのくらいの程度知っていますか。
    
- フォルダーまたはメッセージのプロパティの数はどれだけ移動またはコピーされますか。
    
**imapiprop**メソッドを使用して、フォルダーまたはメッセージのいずれかをコピーまたは移動できます。 **imapifolder:: copymessages**はメッセージのみを処理します。**imapifolder:: copyfolder**はフォルダーのみを使用します。 
  
**imapifolder**メソッドを使用しても、コピーまたは移動するフォルダーやメッセージでサポートされているプロパティを認識する必要はありませんが、 **imapifolder**のメソッドを使用するには、いくつかの知識が必要です。 **imapiprop:: copyprops**を使用すると、コピーまたは移動するフォルダーまたはメッセージのプロパティを明示的に指定できる必要があります。 **imapiprop:: CopyTo**を使用すると、すべてのプロパティをコピーまたは移動するのでない限り、除外する必要があるものを明示的に指定する必要があります。 これらのメソッドの詳細については、「 [MAPI プロパティをコピー](copying-mapi-properties.md)する」を参照してください。
  
コピーまたは移動するプロパティの数は、どのメソッドを使用するかによって決定に影響する場合があります。 複数のメッセージをコピーまたは移動する場合は、 **imapifolder:: copymessages**を呼び出してください。 別の選択肢として、フォルダーの**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) プロパティのみをコピーするのには、 **imapiprop:: copyprops**を呼び出すことをお勧めします。 次の手順は、 **copymessages**の使用方法を示しています。 
  
### <a name="to-copy-or-move-one-or-more-messages"></a>1つまたは複数のメッセージをコピーまたは移動するには
  
1. コピー元とコピー先のフォルダーの有効なエントリ識別子を見つけます。
    
2. これらのフォルダーを読み取り/書き込みモードで開くには、 [imapisession:: openentry](imapisession-openentry.md)または[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出し、MAPI_MODIFY フラグを設定します。 
    
3. **openentry**から返されるインターフェイスポインターが**imapifolder**インターフェイスポインターであることを確認します。 含まれていない場合は、LPMAPIFOLDER 型にキャストします。 
    
4. コピーまたは移動する1つ以上のメッセージを表すエントリ識別子の配列を作成します。 
    
5. 次のフラグが設定された**copymessages:: imapifolder::** を呼び出します。 
    
   - 移動操作を実行する場合は、MESSAGE_MOVE。 
    
   - MESSAGE_DIALOG を使用して、フォルダーで進行状況インジケーターを表示する場合は、 _uluiparam_パラメーターでウィンドウハンドルを渡します。 
    
6. コピー元とコピー先のフォルダーの**imapifolder**ポインターを解放します。 
    
フォルダーの完全なコンテンツを別のフォルダーにコピーする場合は、ソースフォルダーの**imapifolder:: copyfolder**または**imapifolder:: CopyTo**メソッドを呼び出します。 
  
いくつかのフォルダーのプロパティをコピーするには、 **imapiprop:: copyprops**メソッドを呼び出します。 フォルダーのプロパティの大部分をコピーするには、 **imapiprop:: CopyTo**を呼び出します。 
  
たとえば、フォルダーの**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) および**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) プロパティをコピーする場合は、次のオプションがあります。
  
- **imapifolder:: copyfolder**を呼び出して、フォルダーのすべてのプロパティをコピーし、不要なものを新しいフォルダーから削除します。 
    
- **CopyTo**を呼び出して、 **PR_DISPLAY_NAME**と**PR_COMMENT**を除くすべてのフォルダーのプロパティを除外します。 
    
- **PR_DISPLAY_NAME**および**PR_COMMENT**を include 配列に渡して、呼び出し**copyprops**を呼び出します。 
    
この場合、 **copyprops**は、一連のプロパティをコピーするために使用することを意図したものであり、実装するのに最も簡単な方法であるというのが最良の選択です。 
  
フォルダーのプロパティのみをコピーまたは移動するには、メッセージを含めずに、フォルダーの**imapiprop:: CopyTo**メソッドを呼び出し、次のプロパティを除外します。 
  
- **PR_CONTAINER_CONTENTS**([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))
    
- **PR_FOLDER_ASSOCIATED_CONTENTS**([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))
    
copy メソッドは、S_OK を返すことができ、成功の合計、MAPI_W_PARTIAL_COMPLETION、部分的な成功、またはエラーを示します。 MAPI_W_PARTIAL_COMPLETION が返された場合は、 **HR_FAILED**マクロを使用して、より具体的なエラーにアクセスします。 詳細については、「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。
  
メッセージを別のメッセージストアにコピーし、Unicode を両方でサポートしていない場合は、コードページの変換によって情報が失われる可能性があることに注意してください。 通常、メッセージストアが1つまたは両方の形式をサポートしているかどうかを知ることができないため、テキストプロパティを ASCII 文字列としてコピーするか、Unicode 文字列としてコピーするかを決定することはできません。 unicode をサポートしている場合は、unicode コピーを実行してみてください。エラー値 MAPI_E_BAD_CHARWIDTH でエラーが発生した場合は、ASCII にします。
  

