---
title: MAPI �t�H���_�[
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8fac3c92-d2f5-479e-a368-ca82bddd8e30
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 88ddfd9e6bb27abfeee9750c71e98d4fad9d1a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801364"
---
# <a name="mapi-folders"></a>MAPI �t�H���_�[

  
  
**適用されます**: Outlook 
  
フォルダーは、メッセージを組織の基本単位として機能する MAPI オブジェクトです。 階層的に配置すると、メッセージおよびその他のフォルダー、フォルダーは含むことができます。 フォルダーしやすく検索してメッセージを処理します。
  
フォルダーは、 [IMAPIContainer](imapicontainerimapiprop.md)を経由して**IUnknown**インターフェイスと[IMAPIProp](imapipropiunknown.md)インターフェイスから直接継承する[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを実装します。 クライアントは、作成、コピー、およびメッセージとフォルダーを削除するを取得し、メッセージの状態を設定を設定したり、メッセージの読み取りのフラグをオフに**IMAPIFolder**を使用します。 必須メッセージ ストア プロバイダーは、 **IMAPIFolder**内のすべてのメソッドをサポートするために、いくつかの方法を回避する場合は、メッセージ ストア プロバイダーの複雑さのレベルを紹介します。 MAPI では、 [IMAPISupport](imapisupportiunknown.md)インターフェイスでより複雑なフォルダー機能の一部を実装することによりメッセージ ストア プロバイダーによって作業を保存します。 独自のコピー方法を実装するのではなく、メッセージ ストア プロバイダーできますサポート オブジェクトで copy メソッドを呼び出すし、同じ結果を得る。 
  
�t�H���_�[�� 3 ��ނ�����܂��B
  
- ���[�g �t�H���_�[�ɂ��܂��B
    
- �ėp�t�H���_�[�ɂ��܂��B
    
- �t�H���_�[��������܂��B
    
すべてのメッセージ ストアには、少なくとも、ルート フォルダーがあります。 ルート フォルダーは、階層の上に表示され、メッセージ、およびその他のフォルダーが含まれています。 ルート フォルダーことはできません移動、コピー、名前変更、または削除します。 メッセージ ・ ストアごとに 1 つだけのルート フォルダーがあります。
  
他のほとんどのフォルダーは、一般的なフォルダーです。 ルートのフォルダーと同様に汎用的なフォルダーには、メッセージ、およびその他のフォルダーが含まれています。 ルートのフォルダーとは異なり、移動、コピー、名前を変更し、削除します。 ルート フォルダーまたはその他の一般的なフォルダーでは、一般的なフォルダーを作成できます。 クライアントは、別のフォルダーに汎用フォルダーを作成するとき、サブフォルダー、または子のフォルダーに新しいフォルダーが呼び出されます。 新しいフォルダーが置かれているフォルダーは、新しいフォルダーの親フォルダーと呼ばれます。 汎用フォルダーが同じ親フォルダーの兄弟フォルダーと呼びます。 兄弟と兄弟ではないフォルダーの両方または可能性がありますしない一意の名前、メッセージによって、プロバイダーを格納します。 メッセージ ストア プロバイダーをクライアントが同じ親の同じ名前の 2 つのフォルダーを作成しようとすると、MAPI_E_COLLISION のエラー値を返す一意の名前を持つ兄弟フォルダーを必要とします。 
  
検索フォルダーには、一連の定義済みの条件に一致するメッセージへのリンクが含まれています。 検索フォルダーには、実際のメッセージではなく、リンクが含まれている、ため有効で、読み取り専用なのでは。 他のフォルダーが含まれているまたはメッセージまたはフォルダーがあることはできませんが移動またはそれらにコピーします。 それで作成された新しいメッセージがあることはできません。自体ことはできません移動、コピー、または名前を変更します。 検索フォルダーからメッセージが削除されると、実際にメッセージを格納するフォルダーから削除されます。
  
フォルダーの種類は、 **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md)) のプロパティに格納されます。 すべてのフォルダーには、このプロパティの種類に応じて FOLDER_GENERIC、FOLDER_ROOT、または FOLDER_SEARCH のいずれかに設定があります。
  
すべてのフォルダーには、1 つのエントリ id と 1 つのレコードのキーがあります。 エントリ、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) は、識別子はクライアントとサービス ・ プロバイダーによってフォルダーを開きます。 レコードのキー、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) は、他のフォルダーとフォルダーを比較するために使用されるバイナリ値です。 
  
フォルダーには、関連のフォルダーとメッセージ ・ ストアを識別するには、他のプロパティがあります。 次のプロパティは、必要があります。
  
- **PR_PARENT_ENTRYID**([PidTagParentEntryId](pidtagparententryid-canonical-property.md))
    
- **PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))
    
- **PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))
    
いくつかのフォルダーは、ユーザーが実行できる操作の種類を記述する ([PidTagAccess](pidtagaccess-canonical-property.md)) である**PR_ACCESS**プロパティをサポートします。 **PR_ACCESS**の有効な設定の 1 つは MAPI_ACCESS_DELETE で、フォルダーを削除できることを示します。 MAPI_ACCESS_MODIFY、別の設定は、フォルダーを変更できる必要があることを示します。 
  
�K�v�ȃt�H���_�[�̃v���p�e�B�̈ꗗ�́A [IMAPIFolder](imapifolderimapicontainer.md)�C���^�[�t�F�C�X��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[MAPI �A�v���P�[�V�����̊J��](mapi-application-development.md)

