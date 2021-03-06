---
layout: post
title: "2018-03-23周会"
date: 2018-03-23 23:22:20 +0800
description:   # Add post description (optional)
img:  2018-03-23.jpg # Add image post (optional)
list_img:  2018-03-23-list.png
tags: ['week meeting', 'css动画效果', 'js循环']# add tag
---
## 上周codereview执行结果回馈
* **重要的运算都采用php提供的原生函数bcadd,bcdiv,bcmul...对数字进行操作**

```php
    // 代码段1
    $price = $this->CI->price_model->get_by($where);
    $price = (float)$price->value - (float)$transfer->paid_amount;
    $transfer_data['set']['replenishment'] = (float)$price;
    $transfer_data['set']['pay_status'] = 2;
    $transfer_data['set']['total'] = (float)$transfer->total + (float)$price;
    $transfer_data['set']['real_amount'] = (float)$transfer->real_amount + (float)$price;
```

* **$date = get_date(); 同一段代码中防止多次重复调用一个函数，后续只需要使用$date即可**

```php
    // 代码段2
    $tranking_no_data = $this->CI->transfer_model->get_by_from($tracking_table_name, $where_tracking);
    if ($tranking_no_data) {
        //修改数据
        $tracking_data = array(
            'tracking_no'     => $tracking_no->api_order_id,
            'home_no'         => $tracking_no->api_last_mile_code1,
            'added_user_id'   => $added['id'],
            'updated_date'    => get_date(),
        );
        $update_tracking = $this->CI->transfer_model->update_from($tracking_table_name, $where_tracking, $tracking_data);
    } else {
        //拼装渠道跟踪号数据
        $tracking_data = array(
            'order_no'        => $tid,
            'follow_number'   => $follow_number->follow_number,
            'tracking_no'     => $tracking_no->api_order_id,
            'home_no'         => $tracking_no->api_last_mile_code1,
            'added_user_id'   => $added['id'],
            'added_user_name' => $added['real_name'],
            'added_date'      => get_date(),
            'added_ip'        => get_ip(),
            'updated'         => 1,
            'updated_date'    => get_date(),
            'status'          => 1,
        );
        $add_status = $this->CI->transfer_model->insert_to($tracking_table_name, $tracking_data);
    }
```

## 绩效追踪

|  姓名  |   当周  | 占当月 |
|--------|--------|--------|
| 余林   | 95.60%  | 23.90%|
| 何安平 | 100.00% | 25.00%|
| 陈喆   | 144.00% | 36.00%|
| 李彬   | 108.00% | 27.00%|
| 罗鑫   | 153.00% | 38.25%|


## 分享
> 遇到大坑小坑常做记录，周会分享，大家学习，共同进步

* 分享动画和css2D的运用（安平） <a href="../assets/attchment/2018-03-23/anping_share.zip" >点击下载</a>

```
简单形状变化（transform）
Scale （放大）
Translate （移动）
Rotate （旋转）
Skew （斜切）
transform-origin （变化中心）
```

* 陈喆分享 <a href="../assets/attchment/2018-03-23/chenzhe_share.rar" >点击下载</a>

```
layer中的end回调是异步进行
$.grep的使用，从js数组中返回值不等于5的部分
js里循环是可以命名并指定执行
```

* 余林分享 <a href="../assets/attchment/2018-03-23/yulin_share.docx" >点击下载</a>

```
使用下载函数下载文件，出现乱码注意编码
```

* 罗鑫分享 <a href="../assets/attchment/2018-03-23/luoxin_share.docx" >点击下载</a>

```
移动端常见兼容
touchstart, touchmove, touchend
```


## 项目进度
> 会前整理好本周的工作，体现出可实施性。

* FR 3月26日完成新价格设置的上线
* EDK 3月30号之前完成演示测试



## 周会记录
* <a href="../assets/attchment/2018-03-23/mk_content.docx" download="周会记录.docx">周会记录</a>



## 备注
* 下周周会 @罗鑫 提供绩效计算功能
* 下周周会讨论 如何用框架使用的 `OR WHERE` VS `$this->db->or_where`





