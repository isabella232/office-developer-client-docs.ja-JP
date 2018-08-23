---
title: ���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a1c73bb5-b44a-4ec6-89e4-0e2228572b2d
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 235683d8565732034f868dd71e4f2047ffe76f09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569842"
---
# <a name="supporting-named-properties-in-message-stores"></a>���[���̕ۑ��ꏊ�Ŗ��O�t���̃v���p�e�B��T�|�[�g���܂��B

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ オブジェクトは、MAPI によって定義されたプロパティのセットに含まれないことでプロパティを持つことができます。 などのプロパティの名前または名前付きことができます。 名前のないプロパティは、MAPI によって定義されているプロパティの識別子の範囲内になければなりません。 名前付きカスタム プロパティは、MAPI によって定義されているプロパティの識別子の別の範囲に存在します。 カスタム メッセージの種類によって通常使用されます。 メッセージ ストア プロバイダーは、既定のメッセージ ストアとして使用する場合は、名前付きプロパティをサポートしなければなりません。 名前付きプロパティのサポートは、 [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)と[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)のメソッドを実装して、どのような名前を識別する 1 つまたは複数のマッピングの署名を実装することがどのようなプロパティの識別子を持つ移動を意味します。 詳細については、[新しい MAPI プロパティを定義する](defining-new-mapi-properties.md)、[名前付きプロパティのサポート](supporting-named-properties.md)を参照してください。
  
ほとんどのメッセージは、名前付きプロパティ マッピングの 1 つの署名、メッセージ ・ ストア内のすべてのオブジェクトをサポートするプロバイダーを格納します。 2 つの利点があります。 まず、追跡するために 1 つだけを使用する必要がある場合、マッピングの署名を実装する方が簡単です。 第 2 に、メッセージ ・ ストア内のすべてのオブジェクトは、同じマッピング シグネチャを使用している場合クライアント アプリケーションは確実にメッセージ ・ ストア内のメッセージのすべてのプロパティの識別子が同じ名前付きプロパティを実際に参照することです。 これにより、クライアント アプリケーションのフォルダー ビューのインターフェイスの名前付きプロパティの列を表示します。
  
## <a name="see-also"></a>�֘A����



[���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B](implementing-messages-in-message-stores.md)

