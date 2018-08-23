---
title: 'title: "�Y�t�t�@�C����\������e�L�X�g������ݒ��T�|�[�g���܂��B" ms.author: v-tirob author: v-tirob manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview ms.prod: office-online-server localization_priority: Normal api_type:'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816
description: 'COM ms.assetid: 68abe85b-5dc0-40d0-8917-30ea002aa816 description: "�ŏI�X�V��: 2011�N7��23��"'
ms.openlocfilehash: 1b6339d768ac476c24ce988ba761270a50d47464
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580314"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>�Y�t�t�@�C����\������e�L�X�g������ݒ��T�|�[�g���܂��B

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
場所でメッセージの添付ファイルはレンダリングを考慮するクライアント アプリケーションは、メッセージの形式の中にこれらの添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) のプロパティを設定します。 レンダリング配置しないクライアントは、設定を解除このプロパティを残します。
  
�N���C�A���g�ł́A�Y�t�t�@�C���̂��郁�b�Z�[�W���J���A�Y�t�t�@�C������b�Z�[�W�̃e�L�X�g�̏ꏊ�ɕ\�����邩����肷��Y�t�t�@�C���� **PR_RENDERING_POSITION**�v���p�e�B��擾���悤�Ƃ��܂��B�N���C�A���g�́A���̂����ꂩ��g�p���� **PR_RENDERING_POSITION**��擾�ł��܂��B
  
- [PR_RENDERING_POSITION](imapiprop-getprops.md)�v���p�e�B��擾����Y�t�t�@�C����J�� [ **IMAPIProp::GetProps**�ɂ��܂��B 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)�̂ɁA�J���Ă��郁�b�Z�[�W�̓Y�t�t�@�C���̃e�[�u����擾���܂��B **PR_RENDERING_POSITION**�́A�Y�t�t�@�C���̂��ׂẴe�[�u���ŕK�v�ȗ�ł��B����́A�p�t�H�[�}���X����コ���邽�߂ɐ����������@�ł��B 
    
RTF に対応してメッセージ ・ ストアには、 **PR_RENDERING_POSITION**の正確、またはおおよその値を返すかどうかを選択できます。 メッセージ ・ ストアは、メッセージの**PR_BODY**プロパティのメッセージが表示されたら、添付ファイルの**PR_RENDERING_POSITION**値を再計算ため、RTF に対応していないメッセージがいくつか格納だけが保証のレンダリング位置の正確性をクライアントが最初に要求すると**PR_BODY**。 RTF に対応してメッセージ ・ ストアは、パフォーマンスを強化するためにおおよその表示位置の値をクライアントに提供できるのです。 レンダリングの正確な位置ではなく、概算値を提供する時間を節約し、ほとんどの場合だけで十分です。 
  
�N���C�A���g�̃��[�U�[�̐ӔC�ɂ����āA�Y�t�t�@�C���̍쐬���w�肵���l����̋ߎ��l���K�v������́ARTF �Ή����b�Z�[�W�i�[���܂��B���ׂẴN���C�A���g�� **PR_RENDERING_POSITION**��ݒ肷��K�v������܂����A���b�Z�[�W �X�g�A �v���o�C�_�[�́A�x�ɂ̉\����������鏀���ɂȂ�܂��B�N���C�A���g�� **PR_RENDERING_POSITION**���ݒ肳��Ă��Ȃ��Ƃ��Ƀ��b�Z�[�W �X�g�A�悤�ݒ�ł��܂��`��ʒu�����b�Z�[�W�̃e�L�X�g��łȂ����Ƃ����-1 �ɂ��܂��B�N���C�A���g�ɂ���āA���b�Z�[�W��̔C�ӂ̏ꏊ�ɂ���-1 �̕\���ʒu�̓Y�t�t�@�C����\���ł��܂��B�����̃N���C�A���g�ł́A���̃��b�Z�[�W�̏㕔�ɂ���Y�t�t�@�C���̎�ނ�z�u���܂��B
  
**PR_RENDERING_POSITION**プロパティの正確さの度合いは、メッセージ ストアがメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) と ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) である**PR_RTF_COMPRESSED**プロパティの両方を保存するかどうかによって異なりますかのみ**PR_RTF_COMPRESSED**。 **PR_BODY**を生成するクライアントと、メッセージ ・ ストアは、書式設定されたテキストと共に保存、正確な表示位置になります。 ただし、 **PR_RTF_COMPRESSED**のみを保存するため、メッセージ ・ ストアは**PR_BODY**の独自のバージョンを生成する必要がある場合、レンダリング位置しないことをある程度正確なことができます。 これは、クライアントとメッセージ ストア プロバイダーが**PR_BODY**プロパティを生成する方法が異なるのためです。 
  
���m�� **PR_RENDERING_POSITION**�l��v�Z����� RTF �Ή��X�g�A�́A�����ݒ肳�ꂽ�e�L�X�g�ɖ��ߍ��܂�Ă���^�O��g�p���܂��B���[�e�B���e�B�֐� **RTFSync**�́A���̌v�Z����s���āA�Y�t�t�@�C���̕\���ʒu��X�V����ƌĂ΂�邱�Ƃ��ł��܂��B���p�\�ȏ�Ԃ̏��̗ʂɂ���ă��b�Z�[�W �X�g�A�� RTF_SYNC_BODY_CHANGED�ARTF_SYNC_RTF_CHANGED�A�܂��͗����̒l�̂����ꂩ��[��](rtfsync.md)�ɓn�����Ƃ��ł��܂��B
  

