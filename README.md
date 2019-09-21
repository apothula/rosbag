# rosbag
my ros project


I have a rosbag with two topics. when i use rosbag play there were no errors. however i use bag.read_messages() it gives the following error. I am new to ros can help me solving this issue. ros reindex and filter also gives the smae error.

Traceback (most recent call last):
  File "createheader.py", line 11, in <module>
    for topic, msg, t in bag1.read_messages(topics=['gsmsg']):
  File "/opt/ros/melodic/lib/python2.7/dist-packages/rosbag/bag.py", line 2679, in read_messages
    yield self.seek_and_read_message_data_record((entry.chunk_pos, entry.offset), raw, return_connection_header)
  File "/opt/ros/melodic/lib/python2.7/dist-packages/rosbag/bag.py", line 2826, in seek_and_read_message_data_record
    header = _read_header(f)
  File "/opt/ros/melodic/lib/python2.7/dist-packages/rosbag/bag.py", line 2001, in _read_header
    return _build_header_from_str(header, req_op)
  File "/opt/ros/melodic/lib/python2.7/dist-packages/rosbag/bag.py", line 2015, in _build_header_from_str
    raise ROSBagFormatException('Error reading header field: expected %d bytes, read %d' % (size, len(header)))
rosbag.bag.ROSBagFormatException: Error reading header field: expected 38 bytes, read 34
