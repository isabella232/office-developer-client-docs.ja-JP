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
ms.openlocfilehash: 5f03530f994fd13e7dc4c7eaa4124900c28e613b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350702"
---
# <a name="supporting-formatted-text-rendering-attachments"></a>書式付きテキストのサポート: 添付ファイルのレンダリング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ内の添付ファイルがレンダリングされる場所を考慮するクライアントアプリケーションは、メッセージの構成時にこれらの添付ファイルの**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティを設定します。 レンダリングの配置を考慮しないクライアントでは、このプロパティは未設定となります。
  
�N���C�A���g�ł́A�Y�t�t�@�C���̂��郁�b�Z�[�W���J���A�Y�t�t�@�C������b�Z�[�W�̃e�L�X�g�̏ꏊ�ɕ\�����邩����肷��Y�t�t�@�C���� **PR_RENDERING_POSITION**�v���p�e�B��擾���悤�Ƃ��܂��B�N���C�A���g�́A���̂����ꂩ��g�p���� **PR_RENDERING_POSITION**��擾�ł��܂��B
  
- [PR_RENDERING_POSITION](imapiprop-getprops.md)�v���p�e�B��擾����Y�t�t�@�C����J�� [ **IMAPIProp::GetProps**�ɂ��܂��B 
    
- [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)�̂ɁA�J���Ă��郁�b�Z�[�W�̓Y�t�t�@�C���̃e�[�u����擾���܂��B **PR_RENDERING_POSITION**�́A�Y�t�t�@�C���̂��ׂẴe�[�u���ŕK�v�ȗ�ł��B����́A�p�t�H�[�}���X����コ���邽�߂ɐ����������@�ł��B 
    
RTF-aware message stores can choose whether to return an accurate or approximate value for **PR_RENDERING_POSITION**. Because message stores recalculate an attachment's **PR_RENDERING_POSITION** value when asked for the message's **PR_BODY** property, some RTF-aware message stores only guarantee the accuracy of rendering positions when a client asks first for **PR_BODY**. RTF-aware message stores are allowed to provide clients with approximate rendering position values to enhance performance. Providing an approximate rather than an accurate rendering position saves time and is sufficient for most situations. 
  
�N���C�A���g�̃��[�U�[�̐ӔC�ɂ����āA�Y�t�t�@�C���̍쐬���w�肵���l����̋ߎ��l���K�v������́ARTF �Ή����b�Z�[�W�i�[���܂��B���ׂẴN���C�A���g�� **PR_RENDERING_POSITION**��ݒ肷��K�v������܂����A���b�Z�[�W �X�g�A �v���o�C�_�[�́A�x�ɂ̉\����������鏀���ɂȂ�܂��B�N���C�A���g�� **PR_RENDERING_POSITION**���ݒ肳��Ă��Ȃ��Ƃ��Ƀ��b�Z�[�W �X�g�A�悤�ݒ�ł��܂��`��ʒu�����b�Z�[�W�̃e�L�X�g��łȂ����Ƃ����-1 �ɂ��܂��B�N���C�A���g�ɂ���āA���b�Z�[�W��̔C�ӂ̏ꏊ�ɂ���-1 �̕\���ʒu�̓Y�t�t�@�C����\���ł��܂��B�����̃N���C�A���g�ł́A���̃��b�Z�[�W�̏㕔�ɂ���Y�t�t�@�C���̎�ނ�z�u���܂��B
  
**PR_RENDERING_POSITION**プロパティの精度は、メッセージストアがメッセージの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) プロパティと**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) プロパティの両方を保存するかどうかによって決まります。**PR_RTF_COMPRESSED**のみ。 If the client generates **PR_BODY** and the message store saves it along with the formatted text, the rendering positions will be accurate. However, if the message store must generate its own version of **PR_BODY** because it only saves **PR_RTF_COMPRESSED**, it is probable that the rendering positions will be somewhat inaccurate. This is because of the differences in the way that clients and message store providers generate the **PR_BODY** property. 
  
���m�� **PR_RENDERING_POSITION**�l��v�Z����� RTF �Ή��X�g�A�́A�����ݒ肳�ꂽ�e�L�X�g�ɖ��ߍ��܂�Ă���^�O��g�p���܂��B���[�e�B���e�B�֐� **RTFSync**�́A���̌v�Z����s���āA�Y�t�t�@�C���̕\���ʒu��X�V����ƌĂ΂�邱�Ƃ��ł��܂��B���p�\�ȏ�Ԃ̏��̗ʂɂ���ă��b�Z�[�W �X�g�A�� RTF_SYNC_BODY_CHANGED�ARTF_SYNC_RTF_CHANGED�A�܂��͗����̒l�̂����ꂩ��[��](rtfsync.md)�ɓn�����Ƃ��ł��܂��B
  

