---
title: MAPI �A�h���X��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: de63e728fbabf9c153f7a4faa68cad1d7a9331ec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587923"
---
# <a name="mapi-address-book"></a>MAPI �A�h���X��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
統合アドレス帳は、すべてのプロファイルで、アドレス帳プロバイダーからのアドレス指定情報の統合のコレクションにアクセスできるようにするのには MAPI を実装するオブジェクトです。 アドレス帳では、クライアント アプリケーションとサービス ・ プロバイダーはありませんメッセージング システムの一意のアドレス体系を区別します。 代わりに、それらを調べることのすべての受信者のアドレスですべてのメッセージング システムでは、メッセージング システムのアドレス帳プロバイダーがインストールされていれば。
  
アドレス帳は、ユーザーの介入なし、またはコモン ダイアログ ボックスを使用して対話的にプログラムでアクセスできます。 MAPI には、特定の受信者、ユーザーが一意のアドレスと新しいを作成するためのテンプレートのフォームのセットにマップすることはできませんが、受信者を作成するときに、警告に関する詳細情報、アドレス帳のエントリの要約リストを表示するダイアログ ボックスが含まれています。受信者です。
  
MAPI �A�h���X���́A�K�w�\���ɂȂ��Ă��邱�ƂɃ��b�Z�[�W �X�g�A�\����Ɠ����ł��B�A�h���X���́A3 ��ނ̃A�h���X���v���o�C�_�[�ɂ���Ď����I�u�W�F�N�g�ւ̃A�N�Z�X��񋟂��܂��B
  
- �A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B
    
- �z�z���X�g �I�u�W�F�N�g�ł��B
    
- ���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B
    
�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A��ӂ̃G���g�����ʎq����ꂼ��̃I�u�W�F�N�g�̎�ނɃA�N�Z�X���܂��B 
  
���܂��܂Ȏ�ނ̃I�u�W�F�N�g��i�[���邱�ƂŁA�A�h���X���̃R���e�i�[�̓t�H���_�[�Ɏ��Ă��܂��B���̑��̃A�h���X���̃R���e�i�[�Ƃ��ă��b�Z�[�W���O ���[�U�[����єz�z���X�g�̃I�u�W�F�N�g��A�h���X���R���e�i�[��ێ��ł��܂��B�A�h���X���̃I�u�W�F�N�g��ۑ�����A�h���X���̃R���e�i�[��g�p���܂��B
  
アドレス帳の統合された外観を得るには、アドレス帳プロバイダーは、0、1、または、最上位のコンテナーにそれらを結合し、単一の最上位のコンテナーの下の結果を表示する MAPI の詳細を公開します。 アドレス帳プロバイダーは、セッションと別のセットを別のセッションのメッセージの 1 つの種類のコンテナーの 1 つのセットを公開するために選択できます。 アドレス帳プロバイダーが最上位のコンテナーを持たず、受信者を作成するために使用するテンプレートの一覧のみを公開することもできます。
  
���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g��̃I�u�W�F�N�g�́A���b�Z�[�W�̎�M�҂���������Ă��܂��B���b�Z�[�W�̃��[�U�[���X �̎�M�҂ł��B�z�z���X�g�́A��M�҂̃O���[�v�ł��B�e���b�Z�[�W�̃��[�U�[�́A����̃��b�Z�[�W���O �V�X�e���́A����̎�ނ̈�ӂ̃A�h���X������Ă��܂��B�z�z���X�g�́A��M�҂̖��O�t���̃R���N�V�����ł��B�z�z���X�g�ɂ́A���b�Z�[�W�̃��[�U�[ �I�u�W�F�N�g�Ƃ��̑��̔z�z���X�g��܂߂邱�Ƃ��ł��܂��B�N���C�A���g �A�v���P�[�V�����̃��[�U�[�́A�z�z���X�g�Ƀ��b�Z�[�W�𑗐M] ���b�Z�[�W�͊e���X�g�̃��b�Z�[�W�̃��[�U�[�̃����o�[�ɑ��M����邳��܂��B 
  
���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g�̃x�[�X �A�h���X �v���p�e�B�ƌĂ΂�� 5 �̃v���p�e�B�̐ݒ肪����܂��B�����͕K�v�ȃv���p�e�B�ł���A���̂悤�ɊȒP�ɐ�����܂��B
  
|**��{ address �v���p�e�B**|**���**|
|:-----|:-----|
|**PR_ADDRTYPE**([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |��M�҂̃A�h���X����͂��܂��B�e�A�h���X�̎�ނł́A����̌`���Ɉˑ����āA����̃��b�Z�[�W���O �V�X�e�����g���Ă��܂��B  <br/> |
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |��M�҂̖��O��\���\�Ȃł��B  <br/> |
|**PR_EMAIL_ADDRESS**([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |��M�҂̃A�h���X�ł��B  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |�G���g�����ʎq����M�҂ɃA�N�Z�X���邽�߂Ɏg�p���܂��B  <br/> |
|**PR_SEARCH_KEY**([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |�o�C�i�������L�[����M�҂���ʂ��邽�߂Ɏg�p���܂��B  <br/> |
   
MAPI �ł́A�����̃O���[�v�̃x�[�X �A�h���X�̃v���p�e�B�̃o���G�[�V�����̃v���p�e�B���`���܂��B�����̑��̃O���[�v�́A���b�Z�[�W�̃��[�U�[�Ƃ��܂��܂ȏ󋵂ł̔z�z���X�g�ɂ��Đ�����܂��B���Ƃ��΁A�v���p�e�B�� 1 �̃O���[�v�ɂ́A���b�Z�[�W�⑼�̃O���[�v�̑㗝�l�̎�M�҂̑㗝�l�̑��M�҂��ɂ��Đ�����܂��B
  

