#CI  email 使用
email 类文件不动


控制器里的方法内容:
   $config['protocol'] = 'smtp';
          $config['smtp_host'] = 'ssl://smtp.gmail.com';
          $config['smtp_user'] 'chinacodeigniter@gmail.com';
          $config['smtp_pass'] = '**********';
          $config['smtp_port'] = 465;
        $config['charset'] = 'utf-8';
        $config['smtp_timeout'] = 30;
        $config['mailtype'] = 'text';
        $config['wordwrap'] = TRUE;
        $config['crlf']="\\r\\n";  
         $config['newline']="\\r\\n";
         
        $this->load->library('email');

    $this->email->initialize($config);
          
          $this->email->from('chinacodeigniter@gmail.com', '中国共产党');
          $this->email->to('ctv_243028755@qq.com');
          $this->email->subject('明天召开紧急会议');
          $this->email->message('拟定南海问题,人员勿缺!测试,方案!');
          
          $this->email->send();

echo $this->email->print_debugger();
